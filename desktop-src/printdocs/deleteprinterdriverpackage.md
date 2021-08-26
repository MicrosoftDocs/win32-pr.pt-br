---
description: Exclui um pacote de driver de impressora do armazenamento de driver.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Função DeletePrinterDriverPackage (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: d7247f4f0ef4d1f77f00664792d0b7b36bc991b19d437017b54db676731ccc70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112546"
---
# <a name="deleteprinterdriverpackage-function"></a>Função DeletePrinterDriverPackage

Exclui um pacote de driver de impressora do armazenamento de driver.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszServer* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres com terminação nula constante que especifica o nome do servidor de impressão do qual o pacote de driver está sendo excluído. Um **valor de** ponteiro NULL significa o computador local.

</dd> <dt>

*pszInfPath* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres com terminação nula constante que especifica o caminho para o arquivo \* .inf do driver.

</dd> <dt>

*pszEnvironment* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres com terminação nula constante que especifica a arquitetura do processador (por exemplo, Windows NT x86). Pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

S \_ OK, se a operação for bem-sucedida.

E \_ ACCESSDENIED, se o pacote foi fornecido com Windows.

HRESULT \_ CODE(ERROR \_ PRINT DRIVER PACKAGE IN \_ \_ \_ \_ USE), se o pacote estiver sendo usado.

Caso contrário, **o HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [Tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O repositório de driver normalmente é %windir% \\ inf ou %windir% \\ System32 \\ DriverStore \\ FileRepository.

Um pacote de driver que é fornecido com Windows não pode ser removido com essa função.

O usuário deve ter privilégios de administração de impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **DeletePrinterDriverPackageW** (Unicode) e **DeletePrinterDriverPackageA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

