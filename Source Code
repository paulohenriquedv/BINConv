Public Class Form1
    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        Dim Val As String = Nothing
        Dim Result As New System.Text.StringBuilder

        For Each Character As Byte In System.Text.ASCIIEncoding.ASCII.GetBytes(TextBox1.Text)
            Result.Append(Convert.ToString(Character, 2).PadLeft(8, "0"))
            Result.Append(" ")
        Next

        Val = Result.ToString.Substring(0, Result.ToString.Length - 1)
        TextBox2.Text = Val

    End Sub

    Private Sub Button2_Click(sender As Object, e As EventArgs) Handles Button2.Click
        Dim Val As String = Nothing
        Dim Characters As String = System.Text.RegularExpressions.Regex.Replace(TextBox1.Text, "[^01]", "")
        Dim ByteArray((Characters.Length / 8) - 1) As Byte
        For Index As Integer = 0 To ByteArray.Length - 1
            ByteArray(Index) = Convert.ToByte(Characters.Substring(Index * 8, 8), 2)
        Next
        Val = System.Text.ASCIIEncoding.ASCII.GetString(ByteArray)
        TextBox2.Text = Val
    End Sub

    Private Sub Label2_Click(sender As Object, e As EventArgs) Handles Label2.Click
        Me.Close()
    End Sub

    Private Sub Label3_Click(sender As Object, e As EventArgs) Handles Label3.Click
        Me.WindowState = FormWindowState.Minimized
    End Sub
End Class
  
