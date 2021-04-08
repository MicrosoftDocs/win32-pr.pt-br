---
title: Mensagem de TB_GETBITMAPFLAGS (commctrl. h)
description: Recupera os sinalizadores que descrevem o tipo de bitmap a ser usado.
ms.assetid: 64a66fe6-1446-424c-a0c6-388da6a7b081
keywords:
- Controles de TB_GETBITMAPFLAGS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAPFLAGS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e21b5b14fa57d6e454c997cbd0e80ac5716d230e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086530"
---
# <a name="tb_getbitmapflags-message"></a>TB de \_ mensagem GETBITMAPFLAGS

Recupera os sinalizadores que descrevem o tipo de bitmap a ser usado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **DWORD** que descreve o tipo de bitmap que deve ser usado. Se esse valor de retorno tiver o \_ sinalizador grande TBBF, os aplicativos deverão usar bitmaps grandes (24 x 24); caso contrário, os aplicativos deverão usar bitmaps pequenos (16 x 16). Todos os outros bits são reservados.

## <a name="remarks"></a>Comentários

O valor retornado por **TB \_ GETBITMAPFLAGS** é apenas consultor. O controle Toolbar recomenda bitmaps grandes ou pequenos com base no fato de o usuário ter escolhido fontes grandes ou pequenas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





