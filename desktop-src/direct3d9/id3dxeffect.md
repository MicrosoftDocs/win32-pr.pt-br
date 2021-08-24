---
description: Usado para definir e consultar efeitos e para escolher técnicas. Um objeto de efeito pode conter várias técnicas para renderizar o mesmo efeito.
ms.assetid: bffc64ab-12e7-44e9-b296-262b0459a68a
title: Interface ID3DXEffect (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c9f5bdcf90b3e0d317290a569984d1b72d248079de5b3b281325e66af6e443c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119494016"
---
# <a name="id3dxeffect-interface"></a>Interface ID3DXEffect

Usado para definir e consultar efeitos e para escolher técnicas. Um objeto de efeito pode conter várias técnicas para renderizar o mesmo efeito.

## <a name="members"></a>Membros

A interface **ID3DXEffect** herda de [**ID3DXBaseEffect.**](id3dxbaseeffect.md) **ID3DXEffect** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DXEffect** tem esses métodos.



| Método                                                                | Descrição                                                                                                                                                                                      |
|:----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplyParameterBlock**](id3dxeffect--applyparameterblock.md)       | Aplique os valores em um bloco de estado ao estado atual do sistema de efeito.<br/>                                                                                                                 |
| [**Começar**](id3dxeffect--begin.md)                                   | Inicia uma técnica ativa.<br/>                                                                                                                                                           |
| [**BeginParameterBlock**](id3dxeffect--beginparameterblock.md)       | Inicie a captura de alterações de estado em um bloco de parâmetro.<br/>                                                                                                                                   |
| [**BeginPass**](id3dxeffect--beginpass.md)                           | Inicia uma passagem, dentro da técnica ativa.<br/>                                                                                                                                           |
| [**CloneEffect**](id3dxeffect--cloneeffect.md)                       | Cria uma cópia de um efeito.<br/>                                                                                                                                                          |
| [**Commitchanges**](id3dxeffect--commitchanges.md)                   | Propagar alterações de estado que ocorrem dentro de uma passagem ativa para o dispositivo antes da renderização.<br/>                                                                                           |
| [**DeleteParameterBlock**](id3dxeffect--deleteparameterblock.md)     | Exclua um bloco de parâmetro.<br/>                                                                                                                                                             |
| [**End**](id3dxeffect--end.md)                                       | Termina uma técnica ativa.<br/>                                                                                                                                                             |
| [**EndParameterBlock**](id3dxeffect--endparameterblock.md)           | Parar a captura de alterações de estado do parâmetro de efeito.<br/>                                                                                                                                        |
| [**EndPass**](id3dxeffect--endpass.md)                               | Encerrar uma passagem ativa.<br/>                                                                                                                                                                   |
| [**FindNextValidTechnique**](id3dxeffect--findnextvalidtechnique.md) | Pesquisa a próxima técnica válida, começando na técnica após a técnica especificada.<br/>                                                                                       |
| [**GetCurrentTechnique**](id3dxeffect--getcurrenttechnique.md)       | Obtém a técnica atual.<br/>                                                                                                                                                           |
| [**GetDevice**](id3dxeffect--getdevice.md)                           | Recupera o dispositivo associado ao efeito.<br/>                                                                                                                                      |
| [**GetPool**](id3dxeffect--getpool.md)                               | Obtém um ponteiro para o pool de parâmetros compartilhados.<br/>                                                                                                                                      |
| [**GetStateManager**](id3dxeffect--getstatemanager.md)               | Obter o gerenciador de estado de efeito.<br/>                                                                                                                                                         |
| [**IsParameterUsed**](id3dxeffect--isparameterused.md)               | Determina se um parâmetro é usado pela técnica.<br/>                                                                                                                                   |
| [**OnLostDevice**](id3dxeffect--onlostdevice.md)                     | Use esse método para liberar todas as referências a recursos de memória de vídeo e excluir todos os stateblocks. Esse método deve ser chamado sempre que um dispositivo for perdido ou antes de redefinir um dispositivo.<br/> |
| [**OnResetDevice**](id3dxeffect--onresetdevice.md)                   | Use esse método para adquirir recursos e salvar o estado inicial.<br/>                                                                                                                       |
| [**SetRawValue**](id3dxeffect--setrawvalue.md)                       | Definir um intervalo contíguo de constantes de sombreador com uma cópia de memória.<br/>                                                                                                                        |
| [**SetStateManager**](id3dxeffect--setstatemanager.md)               | De definir o gerenciador de estado de efeito.<br/>                                                                                                                                                         |
| [**SetTechnique**](id3dxeffect--settechnique.md)                     | Define a técnica ativa.<br/>                                                                                                                                                            |
| [**ValidateTechnique**](id3dxeffect--validatetechnique.md)           | Validar uma técnica.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A interface ID3DXEffect é obtida chamando [**D3DXCreateEffect**](d3dxcreateeffect.md), [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)ou [**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md).

O tipo LPD3DXEFFECT é definido como um ponteiro para essa interface.


```
typedef interface ID3DXEffect ID3DXEffect;
typedef interface ID3DXEffect *LPD3DXEFFECT;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ID3DXBaseEffect**](id3dxbaseeffect.md)
</dt> <dt>

[Interfaces de efeito](dx9-graphics-reference-effects-interfaces.md)
</dt> <dt>

[**D3DXCreateEffect**](d3dxcreateeffect.md)
</dt> <dt>

[**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md)
</dt> <dt>

[**D3DXCreateEffectFromResource**](d3dxcreateeffectfromresource.md)
</dt> </dl>

 

 




