---
description: Trata o status do dispositivo e as mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: Método IWiaAppErrorHandler::ReportStatus (Wia.h)
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
ms.openlocfilehash: 9cc727845489740fae54dcc96bf5bc903bceb0205688c1c60bee3df980f66845
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965745"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a>Método IWiaAppErrorHandler::ReportStatus

Trata o status do dispositivo e as mensagens de erro durante transferências de dados de imagem e exibe as mensagens para o usuário.

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

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Não usado. Defina como 0.

</dd> <dt>

*pWiaItem2* \[ Em\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Ponteiro para o item que está sendo transferido.

</dd> <dt>

*hrStatus* \[ Em\]
</dt> <dd>

Tipo: **HRESULT**

Código de status do dispositivo.

</dd> <dt>

*lPercentComplete* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Percentual concluído da operação atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Retornará *hrStatus* se a recuperação do erro não for possível. Caso contrário, retornará um dos valores a seguir.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                     | Se *hrStatus* for um erro, a ação apropriada foi tomada para corrigir o erro e a transferência pode continuar. Se *hrStatus* for informativo, o usuário foi informado com uma caixa de diálogo sem modo e optou por não cancelar a transferência.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                  | O usuário cancelou a transferência da caixa de diálogo sem modo do manipulador de erros. Esse valor pode ser retornado a qualquer momento, independentemente do *que seja hrStatus.* <br/>                                                                                      |
| <dl> <dt>**STATUS DO WIA \_ \_ NÃO \_ TRATADO**</dt> </dl> | Nenhuma ação foi tomada; ou seja, nenhuma caixa de diálogo foi apresentada ao usuário. O próximo manipulador de erros será invocado. A ordem dos manipuladores de erros é: aplicativo, driver e padrão do sistema.<br/>                                                 |



 

## <a name="remarks"></a>Comentários

O *parâmetro lPercentComplete* permite que uma janela do manipulador de erros mostre o progresso. Por exemplo, um driver pode fornecer uma estimativa de quanto tempo o "aquecimento" leva. O *parâmetro lPercentComplete* passado para **IWiaAppErrorHandler::ReportStatus** é o mesmo valor que **lPercentComplete** que o driver define na estrutura [**WiaTransferParams.**](-wia-wiatransferparams.md)

Um manipulador de erros pode usar as macros SUCCEEDED e FAILED para descobrir se *hrStatus* tem ERRO DE GRAVIDADE ou \_ ÊXITO DE \_ GRAVIDADE.

Se *hrStatus* for SEVERITY \_ SUCCESS, o usuário deverá ter permissão para cancelar a transferência.

Se *hrStatus* for SEVERITY ERROR, o manipulador de erros deverá exibir uma caixa de diálogo \_ modal pertencente à janela pai do aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




