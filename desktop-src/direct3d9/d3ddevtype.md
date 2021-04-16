---
description: Define os tipos de dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumeração D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761182"
---
# <a name="d3ddevtype-enumeration"></a>Enumeração D3DDEVTYPE

Define os tipos de dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_Hal D3DDEVTYPE**
</dt> <dd>

Rasterização de hardware. O sombreamento é feito com software, hardware ou transformação mista e iluminação.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Inicialize o Direct3D em um computador que não tenha hardware nem que a rasterização de referência esteja disponível e habilite recursos para a criação de conteúdo 3D. Consulte Observações.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ ref**
</dt> <dd>

Os recursos do Direct3D são implementados no software; no entanto, o rasterizador de referência faz uso de instruções de CPU especiais sempre que possível.

O dispositivo de referência é instalado pelo SDK do Windows 8,0 ou posterior e destina-se como uma ajuda na depuração apenas para desenvolvimento.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Um dispositivo de software conectável que foi registrado com [**IDirect3D9:: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ forçar \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar a 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todos os métodos da interface [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) que usam um tipo de dispositivo **D3DDEVTYPE** falharão se D3DDEVTYPE \_ NULLREF for especificado. Para usar esses métodos, substitua D3DDEVTYPE \_ ref na chamada do método.

Um dispositivo de referência de D3DDEVTYPE \_ deve ser criado na memória de rascunho do D3DPOOL \_ , a menos que os buffers de vértice e de índice sejam necessários. Para dar suporte a buffers de vértice e de índice, crie o dispositivo no D3DPOOL \_ SYSTEMMEM Memory.

Se D3dref9.dll estiver instalado, o Direct3D usará o rasterizador de referência para criar um \_ tipo de dispositivo D3DDEVTYPE ref, mesmo se D3DDEVTYPE \_ NULLREF for especificado. Se D3dref9.dll não estiver disponível e D3DDEVTYPE \_ NULLREF for especificado, o Direct3D não será renderizado nem apresentará a cena.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações do Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**\_Parâmetros de criação de D3DDEVICE \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
