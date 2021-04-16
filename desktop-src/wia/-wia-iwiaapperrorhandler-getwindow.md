---
description: Obtém um identificador para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.
ms.assetid: 54deac2e-a395-45dc-b9f9-ecf8140fd9d7
title: 'Método IWiaAppErrorHandler:: GetWindow (WIA. h)'
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
ms.openlocfilehash: 89a3b2bf87d99c767ab3bea46a27c8a53fab7825
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772509"
---
# <a name="iwiaapperrorhandlergetwindow-method"></a>Método IWiaAppErrorHandler:: GetWindow

Obtém um identificador para a caixa de diálogo que exibe mensagens de erro e fornece um ou mais botões para continuar, cancelar ou anular o aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetWindow(
  [out] HWND *phwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*phwnd* \[ fora\]
</dt> <dd>

Tipo: **HWND \** _

HWND usado pelo manipulador de erro do aplicativo, o manipulador de erro do driver e o manipulador de erro padrão para caixas de diálogo de mensagem do dispositivo (erro e informativo). O valor de saída pode ser _ * NULL * *.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

*phwnd* aponta para a janela passada para o [**REPORTSTATUS**](-wia-iwiaerrorhandler-reportstatus.md) pelo proxy WIA (Windows Image Acquisition) 2,0. Essa janela deve permanecer válida durante a transferência de dados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 




