---
description: Obtém um alçamento para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: Método IWiaAppErrorHandler::GetWindow (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.GetWindow
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1bac7ba2f2f9d394218d851f9bbe7939168c2abbc7df5fb8c57a52f29fa6e2b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965755"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>Método IWiaAppErrorHandler::GetWindow

Obtém um alçamento para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phwnd* \[ out\]
</dt> <dd>

Digite: **HWND\***

HWND usado pelo manipulador de erros do aplicativo, pelo manipulador de erros do driver e pelo manipulador de erros padrão para caixas de diálogo de mensagem do dispositivo (erro e informações). O valor de saída pode ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

*phwnd* aponta para a janela passada para [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md) pelo proxy wia (aquisição de imagem) 2.0 do Windows. Essa janela deve permanecer válida durante a transferência de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 




