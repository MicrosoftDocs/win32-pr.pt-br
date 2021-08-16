---
description: Especifica se o modo alfa para tipos de vídeo de mídia de cores é pré-ultado ou direto.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c658cae64c68aa89c49230164707d75369c021767c6aa0b46818516ffa26513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035314"
---
# <a name="mf_mt_alpha_mode-attribute"></a>Atributo \_ MF MT \_ ALPHA \_ MODE

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Especifica se o modo alfa para tipos de vídeo de mídia de cores é pré-ultado ou direto.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor pode ser lançado em um [**valor de MODO \_ ALFA \_ DXGI.**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) Se esse atributo não estiver presente, para compatibilidade com backward, o valor será MODO ALFA DO **DXGI \_ \_ \_ RETA** para o formato de vídeo que dá suporte ao canal alfa, como ARGB32 ou **MODO ALFA DXGI \_ \_ \_ IGNORE** para formato de vídeo sem canal alfa, como RGB32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                      |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
