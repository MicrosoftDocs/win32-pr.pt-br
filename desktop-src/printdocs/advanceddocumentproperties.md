---
description: A função AdvancedDocumentProperties exibe uma caixa de diálogo de configuração de impressora para a impressora especificada, permitindo que o usuário configure essa impressora.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: Função AdvancedDocumentProperties (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 2451f8e0668e0064566511bbf5eeb05e65094967486142719629400cf8d97348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720266"
---
# <a name="advanceddocumentproperties-function"></a>Função AdvancedDocumentProperties

A função **AdvancedDocumentProperties** exibe uma caixa de diálogo de configuração de impressora para a impressora especificada, permitindo que o usuário configure essa impressora.

Essa função é um caso especial da função [**DocumentProperties**](documentproperties.md) . Para obter mais detalhes, consulte a seção comentários.

## <a name="syntax"></a>Sintaxe


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador para a janela pai da caixa de diálogo de configuração da impressora.

</dd> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para um objeto de impressora. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*pDeviceName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo especificando o nome do dispositivo para o qual uma caixa de diálogo de configuração de impressora deve ser exibida.

</dd> <dt>

*pDevModeOutput* \[ fora\]
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que conterá os dados de configuração especificados pelo usuário.

</dd> <dt>

*pDevModeInput* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) que contém os dados de configuração usados para inicializar os controles da caixa de diálogo configuração da impressora.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função [**DocumentProperties**](documentproperties.md) com esses parâmetros for bem-sucedida, o valor de retorno de **AdvancedDocumentProperties** será 1. Caso contrário, o valor de retorno será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Essa função só pode exibir a caixa de diálogo configuração da impressora para que um usuário possa configurá-la. Para obter mais controle, use [**DocumentProperties**](documentproperties.md). Os parâmetros de entrada para essa função são passados diretamente para **DocumentProperties** e o valor de *fMode* é definido como DM \_ no \_ buffer \| DM \_ no \_ prompt \| DM \_ out \_ buffer. Ao contrário de **DocumentProperties**, essa função retorna apenas 1 ou 0. Portanto, você não pode determinar o tamanho necessário de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) definindo *pDevMode* como zero.

Um aplicativo pode obter o nome apontado pelo parâmetro *pDeviceName* chamando a função [**getprinter**](getprinter.md) e, em seguida, examinando o membro **pPrinterName** da estrutura [**\_ info \_ 2 da impressora**](printer-info-2.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **AdvancedDocumentPropertiesW** (Unicode) e **AdvancedDocumentPropertiesA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Informações da impressora \_ \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




