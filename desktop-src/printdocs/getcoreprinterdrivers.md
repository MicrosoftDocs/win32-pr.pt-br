---
description: Recupera o GUID, a versão e a data dos drivers de impressora de núcleo especificados e o caminho para seus pacotes.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Função GetCorePrinterDrivers (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296706"
---
# <a name="getcoreprinterdrivers-function"></a>Função GetCorePrinterDrivers

Recupera o GUID, a versão e a data dos drivers de impressora de núcleo especificados e o caminho para seus pacotes.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
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

*pszzCoreDriverDependencies* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres múltipla terminada em nulo que especifica os GUIDs dos drivers da impressora principal.

</dd> <dt>

*cCorePrinterDrivers* \[ no\]
</dt> <dd>

O número de cadeias de caracteres em *pszzCoreDriverDependencies*.

</dd> <dt>

*pCorePrinterDrivers* \[ fora\]
</dt> <dd>

Um ponteiro para uma matriz de uma ou mais estruturas de [**\_ \_ Driver de impressora principal**](core-printer-driver.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **GetCorePrinterDriversW** (Unicode) e **GetCorePrinterDriversA** (ANSI)<br/>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

