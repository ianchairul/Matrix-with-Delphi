unit Unit1;

interface

uses
  Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
  Dialogs, StdCtrls, Grids, XPMan;

type
  TForm1 = class(TForm)
    StringGrid1: TStringGrid;
    StringGrid2: TStringGrid;
    StringGrid3: TStringGrid;
    Label1: TLabel;
    Label2: TLabel;
    Label3: TLabel;
    Edit1: TEdit;
    Edit2: TEdit;
    Button1: TButton;
    Button2: TButton;
    Label4: TLabel;
    Edit3: TEdit;
    Label5: TLabel;
    Edit4: TEdit;
    RadioButton1: TRadioButton;
    RadioButton2: TRadioButton;
    RadioButton3: TRadioButton;
    XPManifest1: TXPManifest;
    Label6: TLabel;
    Button3: TButton;
    procedure Button1Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure Edit2Change(Sender: TObject);
    procedure Edit1Change(Sender: TObject);
    procedure Edit4Change(Sender: TObject);
    procedure Edit3Change(Sender: TObject);
    procedure Button2Click(Sender: TObject);
  private
    { Private declarations }

  public
    { Public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.dfm}

procedure TForm1.Button1Click(Sender: TObject);
var
  i, j ,k: integer;
  matriksA : array[1..100,1..100] of integer;
  matriksB : array[1..100,1..100] of integer;
  hasilMatriks : array[1..100,1..100] of integer;

begin
//Penjumlahan
  if radiobutton1.Checked then
  begin
  Stringgrid3.Visible:=true;
  stringgrid3.RowCount:=strtoint(edit1.Text)+1;
  stringgrid3.ColCount:=strtoint(edit1.Text)+1;
    for i:=1 to strtoint(edit1.Text) do
    begin
      for j:=1 to strtoint(edit1.Text) do
      begin
      matriksA[i,j]:=strtoint(stringgrid1.Cells[j,i]);
      matriksB[i,j]:=strtoint(stringgrid2.Cells[j,i]);
      hasilMatriks[i,j]:=matriksA[i,j]+matriksB[i,j];
      Stringgrid3.Cells[j,i]:=inttostr(hasilMatriks[i,j]);
      StringGrid3.RowCount := StrtoInt(edit1.Text)+1 ;
      StringGrid3.ColCount := StrtoInt(edit4.Text)+1;
      end;
    end;
  end

//pengurangan
  else if radiobutton2.Checked then
  begin
  stringgrid3.Visible:=true;
  stringgrid3.RowCount:=strtoint(edit1.Text)+1;
  stringgrid3.ColCount:=strtoint(edit2.text)+1;
    for i:=1 to strtoint(edit1.Text) do
    begin
      for j:=1 to strtoint(edit2.Text) do
      begin
      matriksA[i,j]:=strtoint(stringgrid1.cells[j,i]);
      matriksB[i,j]:=strtoint(stringgrid2.Cells[j,i]);
      hasilmatriks[i,j]:=matriksA[i,j]-matriksB[i,j];
      stringgrid3.Cells[j,i]:=inttostr(hasilmatriks[i,j]);
      end;
    end;
  end

//perkalian
  else if radiobutton3.Checked then
  begin
    if ((edit2.Text) = (edit3.Text)) then
    begin
      for i := 1 to StrtoInt(Edit1.Text) do
      for j := 1 to StrtoInt(Edit4.Text) do
      begin
      Hasilmatriks[i,j] := 0;
        for k:= 1 to StrtoInt(Edit2.Text) do
        begin
        matriksA[i,k] := StrtoInt(StringGrid1.Cells[k,i]);
        matriksB[k,j] := StrtoInt(StringGrid2.Cells[j,k]);
        Hasilmatriks [i,j] := Hasilmatriks[i,j] + matriksA[i,k] * matriksB[k,j];

        StringGrid3.RowCount := StrtoInt(edit1.Text)+1 ;
        StringGrid3.ColCount := StrtoInt(edit4.Text)+1;
        end;
      StringGrid3.Cells[j,i] := inttostr(Hasilmatriks[i,j]);
      end;
  end

  else
  begin
  showmessage('Ukuran Matriks Tidak Sesuai');
  edit2.SetFocus;
  end;
end

end;

procedure TForm1.Edit3Change(Sender: TObject);
begin
if( Edit3.Text = EmptyStr) then
stringgrid2.RowCount:=4
else
stringgrid2.RowCount:=strtoint(edit3.text)+1;
end;

procedure TForm1.Edit2Change(Sender: TObject);
begin
if( Edit2.Text = EmptyStr) then
stringgrid1.ColCount:=4
else
stringgrid1.Colcount:=strtoint(edit2.Text)+1;
end;

procedure TForm1.Edit1Change(Sender: TObject);
begin
if( Edit1.Text = EmptyStr) then
stringgrid1.RowCount:=4


else
stringgrid1.RowCount:=strtoint(edit1.Text)+1;
end;

procedure TForm1.Edit4Change(Sender: TObject);
begin
if( Edit4.Text = EmptyStr) then
stringgrid2.ColCount:=4
else
stringgrid2.ColCount:=strtoint(edit4.text)+1;
end;

procedure TForm1.Button3Click(Sender: TObject);
begin
if Application.MessageBox('Are You Sure To Quit?','Caution!!',Mb_YesNo)=ID_yes then form1.Close;
end;

procedure TForm1.Button2Click(Sender: TObject);
var i: integer;
begin
StringGrid3.ColCount:=5;
StringGrid3.RowCount:=5;
Edit1.Clear;
Edit2.Clear;
edit3.Clear;
edit4.Clear;
for i:=0 to StringGrid1.ColCount-1 do
StringGrid1.Cols[i].Clear;
for i:=0 to StringGrid2.ColCount-1 do
StringGrid2.Cols[i].Clear;
for i:=0 to StringGrid3.ColCount-1 do
StringGrid3.Cols[i].Clear;
end;

end.


