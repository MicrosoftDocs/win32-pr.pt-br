---
description: Lida com o status do dispositivo e mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Método IWiaAppErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811658"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>Método IWiaAppErrorHandler:: ReportStatus

Lida com o status do dispositivo e mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Não usado. Defina como 0.

</dd> <dt>

*pWiaItem2* \[ no\]
</dt> <dd>

Tipo: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Ponteiro para o item que está sendo transferido.

</dd> <dt>

_hrStatus * \[ in\]
</dt> <dd>

Tipo: **HRESULT**

Código de status do dispositivo.

</dd> <dt>

*lPercentComplete* \[ no\]
</dt> <dd>

Tipo: **longo**

Porcentagem concluída da operação atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Retorna *hrStatus* se a recuperação do erro não for possível. Caso contrário, ele retorna um dos valores a seguir.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Se *hrStatus* for um erro, a ação apropriada foi executada para corrigir o erro e a transferência poderá continuar. Se *hrStatus* for informativo, o usuário foi informado com uma caixa de diálogo sem janela restrita e optou por não cancelar a transferência.<br/> |
| <dl> <dt>**\_falso**</dt> </dl>                  | O usuário cancelou a transferência da caixa de diálogo sem janela restrita de manipulador de erros. Esse valor pode ser retornado em qualquer ponto, independentemente do que *hrStatus* é. <br/>                                                                                      |
| <dl> <dt>**\_status WIA \_ não \_ Tratado**</dt> </dl> | Nenhuma ação foi executada; ou seja, nenhuma caixa de diálogo foi apresentada ao usuário. O próximo manipulador de erro será invocado. A ordem dos manipuladores de erro é: aplicativo, Driver e padrão do sistema.<br/>                                                 |



 

## <a name="remarks"></a>Comentários

O parâmetro *lPercentComplete* habilita uma janela de manipulador de erros para mostrar o progresso. Por exemplo, um driver pode fornecer uma estimativa de quanto tempo o "aquecimento" leva. O parâmetro *lPercentComplete* passado para **IWiaAppErrorHandler:: ReportStatus** é o mesmo valor que o **lPercentComplete** que o driver define na estrutura [**WiaTransferParams**](-wia-wiatransferparams.md) .

Um manipulador de erro pode usar as macros com êxito e com falha para descobrir se *hrStatus* tem erro de severidade \_ ou êxito na severidade \_ .

Se *hrStatus* for \_ êxito na gravidade, o usuário deverá ter permissão para cancelar a transferência.

Se *hrStatus* for um \_ erro de gravidade, o manipulador de erro deverá exibir uma caixa de diálogo modal pertencente à janela pai do aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




