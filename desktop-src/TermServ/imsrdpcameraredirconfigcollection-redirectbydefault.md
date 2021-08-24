---
title: Propriedade IMsRdpCameraRedirConfigCollection RedirectByDefault
description: Especifica se uma nova câmera é redirecionada ou não por padrão.
ms.tgt_platform: multiple
keywords:
- Propriedade RedirectByDefault Serviços de Área de Trabalho Remota
- A propriedade RedirectByDefault Serviços de Área de Trabalho Remota , interface IMsRdpCameraRedirConfigCollection
- Interface IMsRdpCameraRedirConfigCollection Serviços de Área de Trabalho Remota , propriedade RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8c95431132acf5e3c08ede859520c844c4cae542f6b07dcb8e5781726078e754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475866"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a>Propriedade IMsRdpCameraRedirConfigCollection::RedirectByDefault

Especifica se uma nova câmera é redirecionada ou não por padrão.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a>Valor da propriedade

Um valor que indica se uma nova câmera é redirecionada ou não por padrão.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|---------------------------------------|
| Cliente mínimo com suporte| Windows 10, versão 1803 (build 17134)      |
| Biblioteca de tipos            | MsTscAx.dll                        |
| DLL                  | MsTscAx.dll     |
| IID                      | IID \_ IMsRdpCameraRedirConfigCollection é definido como AE45252B-AAAB-4504-B681-649D6073A37A          |

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpCameraRedirConfigCollection**](imsrdpcameraredirconfigcollection.md)
</dt> </dl>