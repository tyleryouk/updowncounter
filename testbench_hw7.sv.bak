module testbench_hw7 ();

    logic clk, en_b;
    //COMPLETE

    up_down_counter #(
        .N(4)
    ) counter4 (
        .clk    (clk),
        .en_b   (en_b),
        .load_b (load4_b),
        .up     (up),
        .load_in(load_in4),
        .q      (q4),
        .rco_b  (rco4_b)
    );

    up_down_counter #(
        .N(5)
    ) counter5 (
        //COMPLETE
    );

    initial begin
        clk      = 1'b0;
        en_b     = 1'b1;
        load4_b  = 1'b0;
        load5_b  = 1'b0;
        up       = 1'b1;
        load_in4 = 4'b0000;
        load_in5 = 5'b00000;

        forever #5 clk = ~clk;
    end

    initial begin
        #10;
        load4_b = 1'b0;
        load5_b = 1'b0;
        #10;
        en_b = 1'b0;
        #10;
        load4_b = 1'b1;
        load5_b = 1'b1;
        #320;
        en_b     = 1'b1;
        up       = 1'b0;
        load4_b  = 1'b0;
        load5_b  = 1'b0;
        load_in4 = 4'b1111;
        load_in5 = 5'b11111;
        #10;
        en_b = 1'b0;
        #10;
        load4_b = 1'b1;
        load5_b = 1'b1;
        en_b    = 1'b1;
        #10;
        en_b = 1'b0;
        #320;
        load4_b  = 1'b0;
        load5_b  = 1'b0;
        load_in4 = 4'b1010;
        load_in5 = 5'b01010; 
        #10;
        load4_b = 1'b1;
        load5_b = 1'b1;
        #10;
        up       = 1'b1;
        load4_b  = 1'b0;
        load5_b  = 1'b0;
        load_in4 = 4'b0101;
        load_in5 = 5'b10101; 
        #10;
        load4_b = 1'b1;
        load5_b = 1'b1;
        #10;
        $finish();
    end

endmodule
