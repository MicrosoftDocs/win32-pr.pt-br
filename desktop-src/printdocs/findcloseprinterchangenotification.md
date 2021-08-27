---
description: A função FindClosePrinterChangeNotification fecha um objeto de notificação de alteração criado chamando a função FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: Função FindClosePrinterChangeNotification (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 17ec31b1f2992b4311e42e149d39b68b3d724a3d943d67df7c4c5fce88122606
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112486"
---
# <a name="findcloseprinterchangenotification-function"></a>Função FindClosePrinterChangeNotification

A função **FindClosePrinterChangeNotification** fecha um objeto de notificação de alteração criado chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) . A impressora ou o servidor de impressão associado ao objeto de notificação de alteração não será mais monitorado por esse objeto.

## <a name="syntax"></a>Sintaxe


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hChange* \[ no\]
</dt> <dd>

Um identificador para o objeto de notificação de alteração a ser fechado. Trata-se de um identificador criado chamando a função [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

Depois de chamar a função **FindClosePrinterChangeNotification** , você não poderá usar o identificador *hChange* em chamadas subsequentes para [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ou [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md)
</dt> <dt>

[**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md)
</dt> </dl>

 

 




