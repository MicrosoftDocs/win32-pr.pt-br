---
description: Contém informações do driver de impressora.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: DRIVER_INFO_8 (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_8
- _DRIVER_INFO_8A
- _DRIVER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 753b05b9d59bb98742d5c49102b604cc0a499a4dcdc6c624489d261400279297
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118234835"
---
# <a name="driver_info_8-structure"></a>Estrutura INFORMAÇÕES \_ \_ DO DRIVER 8

Contém informações do driver de impressora.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _DRIVER_INFO_8 {
  DWORD     cVersion;
  LPTSTR    pName;
  LPTSTR    pEnvironment;
  LPTSTR    pDriverPath;
  LPTSTR    pDataFile;
  LPTSTR    pConfigFile;
  LPTSTR    pHelpFile;
  LPTSTR    pDependentFiles;
  LPTSTR    pMonitorName;
  LPTSTR    pDefaultDataType;
  LPTSTR    pszzPreviousNames;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  LPTSTR    pszMfgName;
  LPTSTR    pszOEMUrl;
  LPTSTR    pszHardwareID;
  LPTSTR    pszProvider;
  LPTSTR    pszPrintProcessor;
  LPTSTR    pszVendorSetup;
  LPTSTR    pszzColorProfiles;
  LPTSTR    pszInfPath;
  DWORD     dwPrinterDriverAttributes;
  LPTSTR    pszzCoreDriverDependencies;
  FILETIME  ftMinInboxDriverVerDate;
  DWORDLONG dwlMinInboxDriverVerVersion;
} DRIVER_INFO_8, *PDRIVER_INFO_8, *LPDRIVER_INFO_8;
```



## <a name="members"></a>Membros

<dl> <dt>

**cVersion**
</dt> <dd>

A versão do sistema operacional para a qual o driver foi gravado. O valor com suporte é 3.

</dd> <dt>

**Pname**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi gravado (por exemplo, Windows x86, Windows IA64 e Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém dados de driver (por exemplo, C: \\ DRIVERS \\ Qms810.ppd).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo (por exemplo, C: \\ DRIVERS \\ Pscrptui.hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo. Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo de que o driver depende. A sequência de cadeias de caracteres é encerrada por uma cadeia de caracteres vazia de comprimento zero. Se **pDependentFiles** não for **NULL** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de linguagem (por exemplo, "Monitor PJL"). Esse membro pode ser **NULL** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores compatíveis com esse driver. Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

A data do pacote de driver, conforme codificado nos arquivos de driver.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

O número de versão do driver. Isso vem da estrutura de versão do driver.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do fabricante.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL do fabricante.

</dd> <dt>

**pszHardwareID**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a ID de hardware para o driver de impressora.

</dd> <dt>

**pszProvider**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o provedor do driver de impressora (por exemplo, "Microsoft Windows 2000").

</dd> <dt>

**pszPrintProcessor**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o processador de impressão (por exemplo, "WinPrint").

</dd> <dt>

**pszVendorSetup**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a DLL e o ponto de entrada de instalação do driver do fornecedor.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os perfis de cor associados ao driver.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o caminho para o arquivo .inf do driver no armazenamento de driver. (Consulte Comentários.) Isso deverá ser **NULL se** o DRIVER INFO 8 estiver sendo passado para \_ \_ [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx.**](addprinterdriverex.md)

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Sinalizadores de atributo para drivers de impressora. Isso deverá ser 0 se o DRIVER INFO 8 estiver sendo passado para \_ \_ [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx.**](addprinterdriverex.md) Caso contrário, pode ser qualquer combinação dos seguintes sinalizadores:



| Nome/valor do sinalizador                                                         | Significado                                                                                                                                                                                                                                                                                                                                             | Sistema operacional mínimo                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| CIENTE DO \_ PACOTE DO DRIVER DE \_ \_ IMPRESSORA<br/> 0x00000001<br/>        | O driver de impressora faz parte de um pacote de driver.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| XPS \_ DO DRIVER \_ DE IMPRESSORA<br/> 0x00000002<br/>                   | O driver de impressora dá suporte ao formato Microsoft XPS descrito no [XML Paper Specification:](/previous-versions/windows/hardware/design/dn641615(v=vs.85))Visão geral e também na seção Comportamento do Produto, seção [<27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| ÁREA DE \_ TRABALHO DO DRIVER DE IMPRESSORA \_ \_ HABILITADA<br/> 0x00000004<br/>      | O driver de impressora é compatível com o [isolamento do driver de impressora.](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24) Para obter mais informações, consulte [Comportamento do produto, seção <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| CLASSE DE \_ DRIVER \_ DE IMPRESSORA<br/> 0x00000008<br/>                 | O driver de impressora é um [driver de impressora de classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| DRIVER \_ DE \_ IMPRESSORA DERIVADO<br/> 0x00000010<br/>               | O driver de impressora é [um driver de impressora derivado](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| DRIVER DE \_ IMPRESSORA \_ NÃO \_ COMPARTILHÁVEL<br/> 0x00000020<br/>        | Impressoras que usam esse driver de impressora não podem ser compartilhadas.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| FAX DA \_ CATEGORIA DO DRIVER DE \_ \_ IMPRESSORA<br/> 0x00000040<br/>         | O driver de impressora destina-se ao uso com [impressoras de fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| ARQUIVO DE \_ CATEGORIA DE DRIVER DE \_ \_ IMPRESSORA<br/> 0x00000080<br/>        | O driver de impressora destina-se ao uso com [impressoras de arquivo](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
| Categoria de driver de impressora \_ \_ \_ virtual<br/> 0x00000100<br/>     | O driver de impressora destina-se ao uso com [Impressoras virtuais](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_serviço de \_ categoria de driver de impressora \_<br/> 0x00000200<br/>     | O driver de impressora destina-se ao uso com [impressoras de serviço](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                            | Windows 8<br/> Windows Server 2012<br/>    |
| \_redefinição reversível de driver de impressora \_ \_ \_ necessária<br/> 0x00000400<br/> | As impressoras que usam esse driver de impressora devem seguir as diretrizes descritas na definição de classe de dispositivo USB. Para obter mais informações, consulte o [comportamento do produto, seção <36>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43)                                                                      | Windows 8<br/> Windows Server 2012<br/>    |



 

</dd> <dt>

**pszzCoreDriverDependencies**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres múltipla terminada em nulo que especifica todos os drivers de impressora principal dos quais o driver depende. Isso deverá ser **nulo** se as **informações do driver \_ \_ 8** estiverem sendo passadas para [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**ftMinInboxDriverVerDate**
</dt> <dd>

a data mais antiga permitida de quaisquer drivers fornecidos com Windows e com os quais esse driver depende.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

a versão mais antiga permitida de quaisquer drivers fornecidos com Windows e com os quais esse driver depende.

</dd> </dl>

## <a name="remarks"></a>Comentários

As cadeias de caracteres para esses membros estão contidas no arquivo. inf que é usado para adicionar o driver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do driver \_ \_ 8W** (Unicode) e **\_ informações do driver \_ \_ 8a** (ANSI)<br/>                             |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

