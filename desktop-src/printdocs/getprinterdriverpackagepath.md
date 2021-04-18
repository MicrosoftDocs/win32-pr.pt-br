---
description: Recupera o caminho para o pacote de driver de impressora especificado em um servidor de impressão.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Função GetPrinterDriverPackagePath (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785104"
---
# <a name="getprinterdriverpackagepath-function"></a>Função GetPrinterDriverPackagePath

Recupera o caminho para o pacote de driver de impressora especificado em um servidor de impressão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszServer* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão. Use **NULL** para o computador local.

</dd> <dt>

*pszEnvironment* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86). Isso pode ser **nulo**.

</dd> <dt>

*pszLanguage* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o idioma da [interface do usuário multilíngüe](/windows/desktop/Intl/mui-resource-management) para o driver que está sendo instalado. Isso pode ser **nulo**.

</dd> <dt>

*pszPackageID* \[ no\]
</dt> <dd>

Um ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a ID do pacote de driver.

</dd> <dt>

*pszDriverPackageCab* \[ entrada, saída\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o caminho para o arquivo de gabinete para o pacote de driver. Isso pode ser **nulo**. Consulte Observações.

</dd> <dt>

*cchDriverPackageCab* \[ no\]
</dt> <dd>

O tamanho, em caracteres, do buffer *pszDriverPackageCab* . Isso pode ser **nulo**.

</dd> <dt>

*pcchRequiredSize* \[ fora\]
</dt> <dd>

Um ponteiro para o tamanho necessário do buffer *pszDriverPackageCab* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Para obter um valor para *cchDriverPackageCab*, chame a função com **NULL** como o valor de *pszDriverPackageCab*. Use o valor retornado em *pcchRequiredSize* como o valor de *cchDriverPackageCab* e chame a função novamente.

O *pszPackageID* normalmente é obtido de uma chamada para [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **GetPrinterDriverPackagePathW** (Unicode) e **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

