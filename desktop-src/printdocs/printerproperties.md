---
description: A função PrinterProperties exibe uma folha de propriedades da impressora para a impressora especificada.
ms.assetid: 1d4c961b-178b-47af-b983-5b7327919f93
title: Função PrinterProperties (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrinterProperties
api_type:
- DllExport
api_location:
- plotui.dll
- winspool.drv
ms.openlocfilehash: 1b180685154328ad29b9418e1f8d10707067f633d646571ec5ff5fb1dd03a45a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091726"
---
# <a name="printerproperties-function"></a>Função PrinterProperties

A **função PrinterProperties** exibe uma folha de propriedades da impressora para a impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL PrinterProperties(
  _In_ HWND   hWnd,
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWnd* \[ Em\]
</dt> <dd>

Um alça para a janela pai da folha de propriedades.

</dd> <dt>

*hPrinter* \[ Em\]
</dt> <dd>

Um identificador para um objeto de impressora. Use a [**função OpenPrinter**](openprinter.md) [**ou AddPrinter**](addprinter.md) para recuperar um alça de impressora.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>winspool.drv</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Documentproperties**](documentproperties.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




