---
title: Função MsimtfIsWindowFiltered
description: A função MsimtfIsWindowFiltered testa se a janela determinada é filtrada pelo AIMM (Active Input Method Manager).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Função MsimtfIsWindowFiltered Estrutura de Serviços de Texto
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f3841ed5c0436d991d02291c1e395f42d6b31b66f442a3caac0b2062fc27db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476746"
---
# <a name="msimtfiswindowfiltered-function"></a>Função MsimtfIsWindowFiltered

A **função MsimtfIsWindowFiltered** testa se a janela determinada é filtrada pelo AIMM (Active Input Method Manager).

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwnd* \[ Em\]
</dt> <dd>

Um alça de janela a ser testado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado



| Código de retorno                                                                          | Descrição                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Verdade**</dt> </dl>  | Se essa janela for filtrada pelo Gerenciador de Métodos de Entrada Ativo.<br/>     |
| <dl> <dt>**False**</dt> </dl> | Se essa janela não for filtrada pelo Gerenciador de Métodos de Entrada Ativo.<br/> |



 

## <a name="remarks"></a>Comentários

Uma janela pode ser filtrada por IActiveIMMApp::FilterClientWindows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





