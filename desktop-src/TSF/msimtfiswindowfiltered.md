---
title: Função MsimtfIsWindowFiltered
description: A função MsimtfIsWindowFiltered testa se a janela especificada é filtrada por AIMM (Active Input Method Manager).
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Estrutura de serviços de texto da função MsimtfIsWindowFiltered
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
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086128"
---
# <a name="msimtfiswindowfiltered-function"></a>Função MsimtfIsWindowFiltered

A função **MsimtfIsWindowFiltered** testa se a janela especificada é filtrada por AIMM (Active Input Method Manager).

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Um identificador de janela a ser testado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                          | Descrição                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | Se esta janela for filtrada pelo Gerenciador de método de entrada ativo.<br/>     |
| <dl> <dt>**FOR**</dt> </dl> | Se essa janela não for filtrada pelo Gerenciador de método de entrada ativo.<br/> |



 

## <a name="remarks"></a>Comentários

Uma janela pode ser filtrada por IActiveIMMApp:: FilterClientWindows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





