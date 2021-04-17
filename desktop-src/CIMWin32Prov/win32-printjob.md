---
description: Representa um trabalho de impressão gerado por um aplicativo do Windows. Qualquer unidade de trabalho gerada pelo comando Print de um aplicativo que está sendo executado em um computador executando em um sistema operacional Windows é um descendente ou membro dessa classe.
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob
- Win32_PrintJob.Caption
- Win32_PrintJob.Description
- Win32_PrintJob.InstallDate
- Win32_PrintJob.Name
- Win32_PrintJob.Status
- Win32_PrintJob.ElapsedTime
- Win32_PrintJob.JobStatus
- Win32_PrintJob.Notify
- Win32_PrintJob.Owner
- Win32_PrintJob.Priority
- Win32_PrintJob.StartTime
- Win32_PrintJob.TimeSubmitted
- Win32_PrintJob.UntilTime
- Win32_PrintJob.Color
- Win32_PrintJob.DataType
- Win32_PrintJob.Document
- Win32_PrintJob.DriverName
- Win32_PrintJob.HostPrintQueue
- Win32_PrintJob.JobId
- Win32_PrintJob.PagesPrinted
- Win32_PrintJob.PaperLength
- Win32_PrintJob.PaperSize
- Win32_PrintJob.PaperWidth
- Win32_PrintJob.Parameters
- Win32_PrintJob.PrintProcessor
- Win32_PrintJob.Size
- Win32_PrintJob.StatusMask
- Win32_PrintJob.TotalPages
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f56034161a9313eed1b7d302ab790d153c0ee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750947"
---
# <a name="win32_printjob-class"></a>\_Classe PrintJob do Win32

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrintJob do Win32** representa um trabalho de impressão gerado por um aplicativo do Windows. Qualquer unidade de trabalho gerada pelo comando Print de um aplicativo que está sendo executado em um computador executando em um sistema operacional Windows é um descendente ou membro dessa classe.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_PrintJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Color;
  string   DataType;
  string   Document;
  string   DriverName;
  string   HostPrintQueue;
  uint32   JobId;
  uint32   PagesPrinted;
  uint32   PaperLength;
  string   PaperSize;
  uint32   PaperWidth;
  string   Parameters;
  string   PrintProcessor;
  uint32   Size;
  uint32   StatusMask;
  uint32   TotalPages;
};
```

## <a name="members"></a>Membros

A **classe \_ PrintJob do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ PrintJob do Win32** tem esses métodos.



| Método                                                  | Descrição                       |
|:--------------------------------------------------------|:----------------------------------|
| [**Pausar**](pause-method-in-class-win32-printjob.md)   | Pausa um trabalho de impressão.<br/>    |
| [**Retomar**](resume-method-in-class-win32-printjob.md) | Continua um trabalho de impressão.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ PrintJob do Win32** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Uma breve descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Cor**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres que indica se o documento é impresso em cores ou monocromáticas. Algumas impressoras coloridas têm a capacidade de imprimir usando preto em vez de uma combinação de amarelo, ciano e magenta. O verdadeiro preto geralmente cria texto mais escuro e mais nítido para documentos. Essa opção só é útil para impressoras coloridas que dão suporte à impressão em preto real.

Os valores são:

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**Colorida**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**Monocromático**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Formato dos dados para este trabalho de impressão. Isso instrui o driver de impressora a converter os dados (texto genérico, PostScript ou PCL) antes da impressão, ou imprimir em um formato bruto (para elementos gráficos e imagens).

Exemplo: "texto"

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Documento**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do trabalho de impressão. O usuário vê esse nome ao exibir documentos que estão aguardando para serem impressos.

Exemplo: "Microsoft Word-Review.doc"

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do driver de impressora usado para o trabalho de impressão.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Período de tempo em que o trabalho foi executado.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**HostPrintQueue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador no qual o trabalho de impressão é criado.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número do identificador do trabalho. Ele é usado por outros métodos como um identificador para um spool de trabalho para a impressora.

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que representa o status do trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O usuário é notificado após a conclusão ou falha do trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**Proprietário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Usuário que enviou o trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**PagesPrinted**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de páginas que são impressas. Esse valor pode ser 0 (zero) se o trabalho de impressão não contiver informações de delimitação de página.

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimos de milímetro).
</dt> </dl>

Comprimento do papel.

Exemplo: 2794

</dd> <dt>

**Papel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho do papel usado para imprimir o trabalho. O valor é um dos tamanhos de papel possíveis para a impressora especificada na propriedade **PaperSizesSupported** da classe [**de \_ impressora do Win32**](win32-printer.md) .

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimos de milímetro).
</dt> </dl>

Largura do papel.

Exemplo: 2159

</dd> <dt>

**Parâmetros**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Parâmetros opcionais a serem enviados para o processador de impressão. Para obter mais informações, consulte a propriedade do **multiprocessador** .

</dd> <dt>

**Multiprocessador**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Serviço de processador de impressão usado para processar o trabalho de impressão. Um processador de impressora funciona em conjunto com o driver de impressora para fornecer tradução adicional dos dados da impressora para a impressora e também pode ser usado para fornecer opções especiais, como uma página de título para o trabalho.

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Importância da execução de um trabalho.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**Tamanho**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (bytes)
</dt> </dl>

Tamanho do trabalho de impressão.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que o trabalho começou.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "degradado" e "Pred falha". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).

O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço". O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Bitmap dos possíveis status relacionados a esse trabalho de impressão.

<dt>

1 (0x1)
</dt> <dd>

Em Pausa

</dd> <dt>

2 (0x2)
</dt> <dd>

Erro

</dd> <dt>

4 (0x4)
</dt> <dd>

Excluir

</dd> <dt>

8 (0x8)
</dt> <dd>

Spool

</dd> <dt>

16 (0x10)
</dt> <dd>

Imprimindo

</dd> <dt>

32 (0x20)
</dt> <dd>

Offline

</dd> <dt>

64 (0x40)
</dt> <dd>

De papel

</dd> <dt>

128 (0x80)
</dt> <dd>

Exibido

</dd> <dt>

256 (0x100)
</dt> <dd>

Excluído

</dd> <dt>

512 (0x200)
</dt> <dd>

\_DevQ bloqueado

</dd> <dt>

1024 (0x400)
</dt> <dd>

Req. de \_ intervenção do usuário \_

</dd> <dt>

2048 (0x800)
</dt> <dd>

Reiniciar

</dd> </dl>

</dd> <dt>

**Timeenvio**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que o trabalho foi enviado.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> <dt>

**TotalPages**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de páginas necessárias para concluir o trabalho. Esse valor pode ser 0 (zero) se o trabalho de impressão não contiver informações de delimitação de página.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que o trabalho é inválido ou deve ser parado.

Essa propriedade é herdada [**do \_ trabalho CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ PrintJob do Win32** é derivada [**do \_ trabalho CIM**](cim-job.md).

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir descreve como recuperar estatísticas de trabalhos de impressora de instâncias do **Win32 \_ PrintJob**.


```VB
Set PrintJobSet = GetObject("winmgmts:").InstancesOf ("Win32_PrintJob")

If (PrintJobSet.Count = 0) Then WScript.Echo "No print jobs!"
for each PrintJob in PrintJobSet
 WScript.Echo PrintJob.Name
 WScript.Echo PrintJob.JobId
 WScript.Echo PrintJob.Status
 WScript.Echo PrintJob.TotalPages
 Wscript.Echo ""
next
```



O exemplo de código Perl a seguir descreve como recuperar estatísticas de trabalhos de impressora de instâncias do **Win32 \_ PrintJob**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($PrintJobset, $PrintJob);
eval {$PrintJobset = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 InstancesOf ("Win32_PrintJob") };
if (!$@ && defined $PrintJobset)
{
 if ($PrintJobset->{Count} == 0 ) 
 {
  print "\nNo print jobs!\n";
 }

 foreach $PrintJob (in $PrintJobset)
 {
  print $PrintJob->{Name} , "\n";
  print $PrintJob->{JobId} , "\n";
  print $PrintJob->{Status} , "\n";
  print $PrintJob->{TotalPages} , "\n";
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Trabalho do CIM \_**](./cim-job.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
