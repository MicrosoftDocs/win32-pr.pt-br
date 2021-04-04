---
description: Carrega um driver de impressora no repositório de drivers de servidores de impressão para que ele possa ser instalado chamando InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Função UploadPrinterDriverPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171325"
---
# <a name="uploadprinterdriverpackage-function"></a>Função UploadPrinterDriverPackage

Carrega um driver de impressora no repositório de drivers do servidor de impressão para que ele possa ser instalado chamando [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszServer* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão. Use **NULL** se o servidor for o computador local.

</dd> <dt>

*pszInfPath* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o caminho de origem para o arquivo. inf do driver.

</dd> <dt>

*pszEnvironment* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador do servidor (por exemplo, Windows NT x86). Isso pode ser **nulo**.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Isso pode ser qualquer um dos seguintes valores:



| Valor                                                                                                                                                                                     | Significado                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <dt>**UPDP_SILENT_UPLOAD**</dt> </dl>             | A interface do usuário não será mostrada durante o carregamento.<br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <dt>**UPDP_UPLOAD_ALWAYS**</dt> </dl>             | Os arquivos serão carregados mesmo se o pacote já estiver no repositório de drivers do servidor.<br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <dt>**UPDP_CHECK_DRIVERSTORE**</dt> </dl> | O repositório de drivers do servidor será verificado antes do carregamento para ver se o pacote já está lá. Essa configuração será ignorada se UPDP_UPLOAD_ALWAYS estiver definida.<br/> |



 

</dd> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a interface do usuário de cópia.

</dd> <dt>

*pszDestInfPath* \[ fora\]
</dt> <dd>

Um ponteiro para o caminho de destino, no repositório de drivers, ao qual o arquivo. inf do driver foi copiado.

</dd> <dt>

*pcchDestInfPath* \[ entrada, saída\]
</dt> <dd>

Na entrada, especifica o tamanho, em caracteres, do buffer *pszDestInfPath* . Na saída, recebe o tamanho, em caracteres, da cadeia de caracteres do caminho, incluindo o caractere nulo de terminação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será S_OK, caso contrário, o **HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O repositório de drivers normalmente é% windir% \\ inf ou% windir% \\ System32 \\ DriverStore \\ FileRepository.

Somente um pacote por vez pode ser carregado. Se um pacote for dependente de outros, eles deverão ser carregados separadamente.

Somente pacotes de driver assinados podem ser carregados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **UploadPrinterDriverPackageW** (Unicode) e **UploadPrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

