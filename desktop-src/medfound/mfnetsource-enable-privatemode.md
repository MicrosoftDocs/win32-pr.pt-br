---
description: Habilita o modo de download privado na origem da rede.
ms.assetid: 679661A7-1D31-43F3-A64E-16ADCB5414B0
title: MFNETSOURCE_ENABLE_PRIVATEMODE propriedade (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e2ff972aa42753bb92be33fd6bf893d0578f28bf0ad29889a1b5986ba1a77c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113536"
---
# <a name="mfnetsource_enable_privatemode-property"></a>Propriedade MFNETSOURCE \_ ENABLE \_ PRIVATEMODE

Habilita o modo de download privado na origem da rede.



Tipo de dados

Tipo PROPVARIANT (vt)

Membro PROPVARIANT

**Bool**

VT \_ I4

**lVal**



## <a name="remarks"></a>Comentários

Se essa propriedade for **TRUE,** o cache será limpo quando a sessão terminar.

A **constante \_ CLIENTGUID MFNETSOURCE** define o GUID para a chave de propriedade. O PID (identificador de propriedade) é zero. Para definir essa propriedade na origem da rede, passe **um ponteiro IPropertyStore** para o resolvedor de origem. Para obter mais informações, consulte [Configurando uma fonte de mídia](configuring-a-media-source.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




