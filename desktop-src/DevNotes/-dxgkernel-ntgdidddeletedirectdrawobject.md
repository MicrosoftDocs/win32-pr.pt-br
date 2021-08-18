---
description: Destrói um objeto de dispositivo Microsoft DirectDraw no modo kernel criado anteriormente.
ms.assetid: 0b2e1bae-8291-4fe4-9528-980680906e0a
title: Função NtGdiDdDeleteDirectDrawObject (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDeleteDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 866624e35c5c05afa14692a2e83d1c15293af9435aa68deddf9c602b80820708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956545"
---
# <a name="ntgdidddeletedirectdrawobject-function"></a>Função NtGdiDdDeleteDirectDrawObject

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Destrói um objeto de dispositivo Microsoft DirectDraw no modo kernel criado anteriormente.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdDeleteDirectDrawObject(
   HANDLE hDirectDrawLocal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDrawLocal* 
</dt> <dd>

Identificador para o objeto de dispositivo DirectDraw no modo kernel.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedida, essa função **retornará TRUE;** caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

Os aplicativos são aconselhados a usar as APIs DirectDraw e [Direct3D](../direct3d10/d3d10-graphics-reference.md) para criar e gerenciar objetos de dispositivo gráfico. Esses constructos abstraem o processo de criação do dispositivo de maneira simplificada e independente do sistema operacional.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**NtGdiDdCreateDirectDrawObject**](-dxgkernel-ntgdiddcreatedirectdrawobject.md)
</dt> <dt>

[**DdDeleteDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-dddeletedirectdrawobject)
</dt> </dl>

 

 
