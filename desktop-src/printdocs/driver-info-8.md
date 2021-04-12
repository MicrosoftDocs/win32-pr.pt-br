---
description: Contém informações de driver de impressora.
ms.assetid: 6237def2-ffd4-4d93-b3a4-56f225793457
title: Estrutura de DRIVER_INFO_8 (winspool. h)
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
ms.openlocfilehash: 3cc174fdc8617a8ff59afc5a12740eaba715114f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297467"
---
# <a name="driver_info_8-structure"></a>Estrutura de informações de DRIVER \_ \_ 8

Contém informações de driver de impressora.

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

**pName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver (por exemplo, QMS 810).

</dd> <dt>

**pEnvironment**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente para o qual o driver foi escrito (por exemplo, Windows x86, Windows IA64 e Windows x64.

</dd> <dt>

**pDriverPath**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém o driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscript.dll).

</dd> <dt>

**pDataFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo que contém os dados do driver (por exemplo, C: \\ drivers \\ Qms810. PPD).

</dd> <dt>

**pConfigFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para a biblioteca de vínculo dinâmico de configuração do driver de dispositivo (por exemplo, C: \\ DRIVERS \\Pscrptui.dll).

</dd> <dt>

**pHelpFile**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um nome de arquivo ou um caminho completo e um nome de arquivo para o arquivo de ajuda do driver de dispositivo (por exemplo, C: \\ drivers \\ pscrptui. hlp).

</dd> <dt>

**pDependentFiles**
</dt> <dd>

Um ponteiro para um buffer MultiSZ que contém uma sequência de cadeias de caracteres terminadas em nulo. Cada cadeia de caracteres terminada em nulo no buffer contém o nome de um arquivo do qual o driver depende. A sequência de cadeias de caracteres é terminada por uma cadeia de caracteres vazia e de comprimento zero. Se **pDependentFiles** não for **nulo** e não contiver nenhum nome de arquivo, ele apontará para um buffer que contém duas cadeias de caracteres vazias.

</dd> <dt>

**pMonitorName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica um monitor de idioma (por exemplo, "Monitor de PJL"). Esse membro pode ser **nulo** e deve ser especificado somente para impressoras com capacidade de comunicação bidirecional.

</dd> <dt>

**pDefaultDataType**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o tipo de dados padrão do trabalho de impressão (por exemplo, "EMF").

</dd> <dt>

**pszzPreviousNames**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica nomes de driver de impressora anteriores que são compatíveis com este driver. Por exemplo, OldName1 \\ 0OldName2 \\ 0 \\ 0.

</dd> <dt>

**ftDriverDate**
</dt> <dd>

A data do pacote de driver, conforme codificado nos arquivos de driver.

</dd> <dt>

**dwlDriverVersion**
</dt> <dd>

O número de versão do driver. Isso é proveniente da estrutura de versão do driver.

</dd> <dt>

**pszMfgName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do fabricante.

</dd> <dt>

**pszOEMUrl**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a URL para o fabricante.

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

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica a DLL de instalação do driver do fornecedor e o ponto de entrada.

</dd> <dt>

**pszzColorProfiles**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica os perfis de cor associados ao driver.

</dd> <dt>

**pszInfPath**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o caminho para o arquivo. inf do driver no repositório de drivers. (Consulte comentários.) Isso deverá ser **nulo** se as informações do driver \_ \_ 8 estiverem sendo passadas para [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md).

</dd> <dt>

**dwPrinterDriverAttributes**
</dt> <dd>

Sinalizadores de atributo para drivers de impressora. Isso deve ser 0 se as informações de DRIVER \_ \_ 8 estiverem sendo passadas para [**AddPrinterDriver**](addprinterdriver.md) ou [**AddPrinterDriverEx**](addprinterdriverex.md). Caso contrário, pode ser qualquer combinação dos seguintes sinalizadores:



| Nome/valor do sinalizador                                                         | Significado                                                                                                                                                                                                                                                                                                                                             | Sistema operacional mínimo                                             |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| \_reconhecimento de \_ pacote de driver de impressora \_<br/> 0x00000001<br/>        | O driver de impressora faz parte de um pacote de driver.                                                                                                                                                                                                                                                                                                     | Windows Vista                                          |
| Driver de impressora \_ \_ XPS<br/> 0x00000002<br/>                   | O driver de impressora dá suporte ao formato XPS da Microsoft descrito no [XML Paper Specification: visão geral](/previous-versions/windows/hardware/design/dn641615(v=vs.85))e também no [comportamento do produto, seção <27>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43).                        | Windows 8<br/> Windows Server 2012<br/>    |
| \_área restrita do driver de impressora \_ \_ habilitada<br/> 0x00000004<br/>      | O driver de impressora é compatível com o [isolamento de driver de impressora](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24). Para obter mais informações, consulte o [comportamento do produto, seção <28>](/openspecs/windows_protocols/ms-rprn/e81cbc09-ab05-4a32-ae4a-8ec57b436c43). | Windows 7<br/> Windows Server 2008 R2<br/> |
| \_classe de driver de impressora \_<br/> 0x00000008<br/>                 | O driver de impressora é um [Driver de impressora de classe](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                       | Windows 8<br/> Windows Server 2012<br/>    |
| Driver de impressora \_ \_ derivado<br/> 0x00000010<br/>               | O driver de impressora é um [Driver de impressora derivado](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                   | Windows 8<br/> Windows Server 2012<br/>    |
| Driver de impressora \_ \_ não \_ compartilhável<br/> 0x00000020<br/>        | As impressoras que usam este driver de impressora não podem ser compartilhadas.                                                                                                                                                                                                                                                                                                | Windows 8<br/> Windows Server 2012<br/>    |
| \_fax de \_ categoria de driver de impressora \_<br/> 0x00000040<br/>         | O driver de impressora destina-se ao uso com [impressoras de fax](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                    | Windows 8<br/> Windows Server 2012<br/>    |
| \_arquivo de \_ categoria do driver de impressora \_<br/> 0x00000080<br/>        | O driver de impressora destina-se ao uso com [impressoras de arquivo](/openspecs/windows_protocols/ms-rprn/831cd729-be7c-451e-b729-bd8d84ce4d24).                                                                                                                                                                                  | Windows 8<br/> Windows Server 2012<br/>    |
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

A data mais antiga permitida de quaisquer drivers fornecidos com o Windows e com os quais esse driver depende.

</dd> <dt>

**dwlMinInboxDriverVerVersion**
</dt> <dd>

A versão mais antiga permitida de quaisquer drivers fornecidos com o Windows e com os quais esse driver depende.

</dd> </dl>

## <a name="remarks"></a>Comentários

As cadeias de caracteres para esses membros estão contidas no arquivo. inf que é usado para adicionar o driver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **\_ Informações do driver \_ \_ 8W** (Unicode) e **\_ informações do driver \_ \_ 8a** (ANSI)<br/>                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Estruturas de API do spooler de impressão](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddPrinterDriver**](addprinterdriver.md)
</dt> <dt>

[**AddPrinterDriverEx**](addprinterdriverex.md)
</dt> </dl>

 

