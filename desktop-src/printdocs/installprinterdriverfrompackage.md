---
description: Instala um driver de impressora de um pacote de driver que está no repositório de drivers de servidores de impressão.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Função InstallPrinterDriverFromPackage (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171708"
---
# <a name="installprinterdriverfrompackage-function"></a>Função InstallPrinterDriverFromPackage

Instala um driver de impressora de um pacote de driver que está no repositório de drivers do servidor de impressão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszServer* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão. **NULL** significa o computador local.

</dd> <dt>

*pszInfPath* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o caminho do repositório de drivers para o arquivo. inf do driver de impressão. **NULL** significa que o driver está em um arquivo inf fornecido com o Windows.

</dd> <dt>

*pszDriverName* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do driver.

</dd> <dt>

*pszEnvironment* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86). Isso pode ser **nulo**.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Isso pode ser somente 0 ou IPDFP \_ copiar \_ todos os \_ arquivos. Um valor de 0 significa que o driver de impressora deve ser adicionado e todos os arquivos no diretório de driver de impressora mais novos do que os arquivos correspondentes atualmente em uso devem ser copiados. Um valor de IPDFP \_ copiar \_ todos os \_ arquivos significa que o driver de impressora e todos os arquivos no diretório do driver de impressora devem ser adicionados. Os carimbos de data/hora do arquivo são ignorados quando *dwFlags* tem um valor de IPDFP \_ copiar \_ todos os \_ arquivos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O repositório de drivers normalmente é% windir% \\ inf ou% windir% \\ System32 \\ DriverStore \\ FileRepository.

O **InstallPrinterDriverFromPackage** também instala outros arquivos no pacote, como perfis de cor e processadores de impressão.

Os usuários devem ter direitos de administração de impressora para serem instalados em um computador remoto ou no computador local quando o usuário estiver conectado com os serviços de terminal.

Somente pacotes assinados podem ser instalados em um computador remoto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **InstallPrinterDriverFromPackageW** (Unicode) e **InstallPrinterDriverFromPackageA** (ANSI)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

