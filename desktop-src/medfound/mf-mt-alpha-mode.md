---
description: Especifica se o modo alfa para tipos de vídeo de mídia de cor é premultiplicado ou reto.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Atributo MF_MT_ALPHA_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011099"
---
# <a name="mf_mt_alpha_mode-attribute"></a>\_Atributo de \_ \_ modo alfa do MF MT

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Especifica se o modo alfa para tipos de vídeo de mídia de cor é premultiplicado ou reto.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse valor pode ser convertido em um valor de [**\_ \_ modo alfa dxgi**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) . Se esse atributo não estiver presente, para compatibilidade com versões anteriores, o valor será o **\_ modo alfa de dxgi \_ \_ direto** para formato de vídeo com suporte para o canal alfa, como ARGB32 ou o **\_ modo alfa de dxgi \_ \_ ignorar** para formato de vídeo sem canal alfa, como RGB32.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                      |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
