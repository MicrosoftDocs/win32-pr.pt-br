---
description: A \_ estrutura de dados informações de notificação de impressora \_ \_ identifica um campo de informações de trabalho ou impressora e fornece os dados atuais para esse campo.
ms.assetid: 7a7b9e01-32e0-47f8-a5b1-5f7e6a663714
title: Estrutura de PRINTER_NOTIFY_INFO_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO_DATA,
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4c76ffe70a8388e920b5f8576830e31ed23edc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169932"
---
# <a name="printer_notify_info_data-structure"></a>\_Estrutura de \_ dados de informações de notificação de impressora \_

A estrutura de **\_ \_ \_ dados informações de notificação de impressora** identifica um campo de informações de trabalho ou impressora e fornece os dados atuais para esse campo.

A função [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) retorna uma estrutura de [**\_ \_ informações de notificação de impressora**](printer-notify-info.md) , que contém uma matriz de estruturas de **\_ \_ \_ dados de informações de notificação de impressora** .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PRINTER_NOTIFY_INFO_DATA {
  WORD  Type;
  WORD  Field;
  DWORD Reserved;
  DWORD Id;
  union {
    DWORD  adwData[2];
    struct {
      DWORD  cbBuf;
      LPVOID pBuf;
    } Data;
  } NotifyData;
} PRINTER_NOTIFY_INFO_DATA, *PPRINTER_NOTIFY_INFO_DATA; ;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Indica o tipo de informação fornecido. Esse membro pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                                      | Significado                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <dt>**Trabalho \_ do NOTIFICAr \_ tipo**</dt> <dt>0x01</dt> </dl>             | Indica que o membro de **campo** especifica uma \_ constante de campo de notificação de trabalho \_ \_ \* .<br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <dt>**Impressora \_ NOTIFICAr \_ tipo**</dt> <dt>0x00</dt> </dl> | Indica que o membro de **campo** especifica uma \_ constante de campo de notificação de impressora \_ \_ \* .<br/> |



 

</dd> <dt>

**Campo**
</dt> <dd>

Indica o campo que foi alterado. Para obter uma lista de valores possíveis, consulte a seção comentários.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> <dt>

**Id**
</dt> <dd>

Indica o identificador de trabalho se o membro de **tipo** especificar o tipo de notificação de trabalho \_ \_ . Se o **tipo** membro especificar \_ \_ tipo de notificação de impressora, esse membro será indefinido.

</dd> <dt>

**NotifyData**
</dt> <dd>

Uma União de informações de dados com base nos membros de **tipo** e **campo** . Para obter uma descrição do tipo de dados associado a cada campo, consulte a seção comentários.

<dl> <dt>

**adwData \[ 2\]**
</dt> <dd>

Uma matriz de dois valores **DWORD** . Para campos de informações que usam apenas uma única **DWORD**, os dados estão em **adwData** \[ 0 \] .

</dd> <dt>

**Dados**
</dt> <dd> <dl> <dt>

**cbBuf**
</dt> <dd>

Indica o tamanho, em bytes, do buffer apontado por **pBuf**.

</dd> <dt>

**pBuf**
</dt> <dd>

Ponteiro para um buffer que contém os dados atuais do campo.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Se o **tipo** membro especificar \_ tipo de notificação de impressora \_ , o membro de **campo** poderá ser um dos valores a seguir.



<table>
<thead>
<tr class="header">
<th>Campo</th>
<th>Tipo de dados</th>
<th>Valor</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SERVER_NAME</td>
<td>Não há suporte.</td>
<td>0x00</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINTER_NAME</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora.</td>
<td>0x01</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SHARE_NAME</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que identifica o ponto de compartilhamento da impressora.</td>
<td>0x02</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PORT_NAME</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da porta na qual os trabalhos de impressão serão impressos. Se &quot; &quot; o pool de impressoras estiver selecionado, essa será uma lista de portas separadas por vírgula.</td>
<td>0x03</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_DRIVER_NAME</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome do driver da impressora.</td>
<td>0x04</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_COMMENT</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém a nova cadeia de caracteres de comentário, que normalmente é uma breve descrição da impressora.</td>
<td>0x05</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_LOCATION</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o novo local físico da impressora (por exemplo, &quot; Bldg. 38, sala 1164 &quot; ).</td>
<td>0x06</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEVMODE</td>
<td><strong>pBuf</strong> é um ponteiro para uma estrutura <a href="/windows/win32/api/wingdi/ns-wingdi-devmodea"><strong>DEVMODE</strong></a> que define dados de impressora padrão, como a orientação do papel e a resolução.</td>
<td>0x07</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SEPFILE</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do arquivo usado para criar a página separadora. Esta página é usada para separar trabalhos de impressão enviados para a impressora.</td>
<td>0x08</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PRINT_PROCESSOR</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão usado pela impressora.</td>
<td>0x09</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PARAMETERS</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros de processador de impressão padrão.</td>
<td>0x0A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DATATYPE</td>
<td><strong>pBuf</strong> é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.</td>
<td>0x0B</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_SECURITY_DESCRIPTOR</td>
<td><strong>pBuf</strong> é um ponteiro para uma estrutura de <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> para a impressora. O ponteiro pode ser <strong>nulo</strong> se não houver nenhum descritor de segurança.</td>
<td>0x0C</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_ATTRIBUTES</td>
<td><strong>adwData</strong> [0] Especifica os atributos da impressora, que podem ser um dos seguintes valores:<dl> PRINTER_ATTRIBUTE_QUEUED<br />
PRINTER_ATTRIBUTE_DIRECT<br />
PRINTER_ATTRIBUTE_DEFAULT<br />
PRINTER_ATTRIBUTE_SHARED<br />
</dl></td>
<td>0x0D</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_PRIORITY</td>
<td><strong>adwData</strong> [0] Especifica um valor de prioridade que o spooler usa para rotear trabalhos de impressão.</td>
<td>0x0E</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_DEFAULT_PRIORITY</td>
<td><strong>adwData</strong> [0] Especifica o valor de prioridade padrão atribuído a cada trabalho de impressão.</td>
<td>0x0F</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_START_TIME</td>
<td><strong>adwData</strong> [0] Especifica a hora mais antiga em que a impressora imprimirá um trabalho. (Esse valor é especificado em minutos decorridos desde 12:00 A.M.)</td>
<td>0x10</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_UNTIL_TIME</td>
<td><strong>adwData</strong> [0] Especifica a hora mais recente em que a impressora imprimirá um trabalho. (Esse valor é especificado em minutos decorridos desde 12:00 A.M.)</td>
<td>0x11</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_STATUS</td>
<td><strong>adwData</strong> [0] Especifica o status da impressora. Para obter uma lista de valores possíveis, consulte a estrutura de <a href="printer-info-2.md"><strong>PRINTER_INFO_2</strong></a> .</td>
<td>0x12</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_STATUS_STRING</td>
<td>Não há suporte.</td>
<td>0x13</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_CJOBS</td>
<td><strong>adwData</strong> [0] Especifica o número de trabalhos de impressão que foram enfileirados para a impressora.</td>
<td>0x14</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_AVERAGE_PPM</td>
<td><strong>adwData</strong> [0] Especifica o número médio de páginas por minuto que foram impressas na impressora.</td>
<td>0x15</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_PAGES</td>
<td>Não há suporte.</td>
<td>0x16</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_PAGES_PRINTED</td>
<td>Não há suporte.</td>
<td>0x17</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_TOTAL_BYTES</td>
<td>Não há suporte.</td>
<td>0x18</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_BYTES_PRINTED</td>
<td>Não há suporte.</td>
<td>0x19</td>
</tr>
<tr class="odd">
<td>PRINTER_NOTIFY_FIELD_OBJECT_GUID</td>
<td>Isso será definido se o GUID do objeto for alterado.</td>
<td>0x1A</td>
</tr>
<tr class="even">
<td>PRINTER_NOTIFY_FIELD_FRIENDLY_NAME</td>
<td>Isso será definido se a conexão de impressora for renomeada.</td>
<td>0x1B</td>
</tr>
</tbody>
</table>



 

Se o membro de **tipo** especificar o tipo de notificação de trabalho \_ \_ , o **campo** membro poderá ser um dos valores a seguir.



| Campo                                    | Tipo de dados                                                                                                                                                                                                                                            | Valor |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| \_nome da \_ impressora do campo NOTIFICAr trabalho \_ \_        | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que contém o nome da impressora para a qual o trabalho está no spool.                                                                                                                                      | 0x00  |
| \_nome da \_ máquina do campo de notificação de trabalho \_ \_        | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do computador que criou o trabalho de impressão.                                                                                                                                    | 0x01  |
| \_nome da \_ porta do campo NOTIFICAr trabalho \_ \_           | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que identifica as portas usadas para transmitir dados para a impressora. Se uma impressora estiver conectada a mais de uma porta, os nomes das portas serão separados por vírgulas (por exemplo, "LPT1:, LPT2:, LPT3:"). | 0x02  |
| \_nome de \_ usuário do campo de notificação de trabalho \_ \_           | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que enviou o trabalho de impressão.                                                                                                                                           | 0x03  |
| \_nome da \_ notificação do campo de notificação de trabalho \_ \_         | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do usuário que deve ser notificado quando o trabalho tiver sido impresso ou quando ocorrer um erro durante a impressão do trabalho.                                                              | 0x04  |
| \_tipo de \_ dados do campo de notificação de trabalho \_             | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados usado para registrar o trabalho de impressão.                                                                                                                                         | 0x05  |
| \_processador de \_ impressão de campo de notificação de trabalho \_ \_     | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do processador de impressão a ser usado para imprimir o trabalho.                                                                                                                           | 0x06  |
| \_parâmetros de \_ campo de notificação de trabalho \_           | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os parâmetros do processador de impressão.                                                                                                                                                            | 0x07  |
| \_nome do \_ Driver do campo NOTIFICAr trabalho \_ \_         | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver de impressora que deve ser usado para processar o trabalho de impressão.                                                                                                           | 0x08  |
| \_DEVMODE do \_ campo de notificação de trabalho \_              | **pBuf** é um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém dados de inicialização de dispositivo e de ambiente para o driver de impressora.                                                                                                        | 0x09  |
| \_status do \_ campo de notificação de trabalho \_               | **adwData** \[ 0 \] especifica o status do trabalho. Para obter uma lista de valores possíveis, consulte a estrutura [**informações do trabalho \_ \_ 2**](job-info-2.md) .                                                                                                                        | 0x0A  |
| \_cadeia de \_ status do campo NOTIFICAr trabalho \_ \_       | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o status do trabalho de impressão.                                                                                                                                                           | 0x0B  |
| \_ \_ \_ descritor de segurança do campo de notificação de trabalho \_ | Não há suporte.                                                                                                                                                                                                                                          | 0x0C  |
| \_documento de \_ campo de notificação de trabalho \_             | **pBuf** é um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do trabalho de impressão (por exemplo, "MS-WORD: Review.doc").                                                                                                                        | 0x0D  |
| \_prioridade do \_ campo de notificação de trabalho \_             | **adwData** \[ 0 \] especifica a prioridade do trabalho.                                                                                                                                                                                                           | 0x0E  |
| \_posição do \_ campo de notificação de trabalho \_             | **adwData** \[ 0 \] especifica a posição do trabalho na fila de impressão.                                                                                                                                                                                      | 0x0F  |
| campo de notificação de trabalho \_ \_ \_ enviado            | **pBuf** é um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que especifica a hora em que o trabalho foi enviado.                                                                                                                          | 0x10  |
| \_hora de \_ início do campo NOTIFICAr trabalho \_ \_          | **adwData** \[ 0 \] especifica a hora mais antiga em que o trabalho pode ser impresso. (Esse valor é especificado em minutos decorridos desde 12:00 A.M.)                                                                                                                | 0x11  |
| campo de notificação de trabalho \_ \_ até a \_ \_ hora          | **adwData** \[ 0 \] especifica a hora mais recente em que o trabalho pode ser impresso. (Esse valor é especificado em minutos decorridos desde 12:00 A.M.)                                                                                                                  | 0x12  |
| \_hora do \_ campo de notificação de trabalho \_                 | **adwData** \[ 0 \] especifica o tempo total, em segundos, decorrido desde que o trabalho começou a ser impresso.                                                                                                                                                  | 0x13  |
| TOTAL de páginas de notificação de trabalho do \_ \_ campo \_ \_         | **adwData** \[ 0 \] especifica o tamanho, em páginas, do trabalho.                                                                                                                                                                                             | 0x14  |
| páginas de campo de notificação de trabalho \_ \_ \_ \_ impressas       | **adwData** \[ 0 \] especifica o número de páginas que foram impressas.                                                                                                                                                                                      | 0x15  |
| \_total de \_ bytes do campo de notificação de trabalho \_ \_         | **adwData** \[ 0 \] especifica o tamanho, em bytes, do trabalho.                                                                                                                                                                                             | 0x16  |
| BYTES de campo de notificação de trabalho \_ \_ \_ \_ impressos       | **adwData** \[ 0 \] especifica o número de bytes que foram impressos neste trabalho. Para esse campo, o objeto de notificação de alteração é sinalizado quando bytes são enviados para a impressora.                                                                      | 0x17  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> <dt>

[**Informações do trabalho \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> <dt>

[**\_informações de notificação da impressora \_**](printer-notify-info.md)
</dt> <dt>

[**\_descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)
</dt> </dl>

