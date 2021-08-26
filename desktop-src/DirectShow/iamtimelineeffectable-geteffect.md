---
description: O método GetEffect recupera o efeito no nível de prioridade especificado.
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'Método IAMTimelineEffectable:: GetEffect (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d53ecc7c3d5291ddb6b894b24835eeb236f036e94eb166383da907a9f469c960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905176"
---
# <a name="iamtimelineeffectablegeteffect-method"></a>Método IAMTimelineEffectable:: GetEffect

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O método **GetEffect** recupera o efeito no nível de prioridade especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppFX* \[ fora\]
</dt> <dd>

Recebe a interface [**IAMTimelineObj**](iamtimelineobj.md) do efeito.

</dd> <dt>

*Onde* 
</dt> <dd>

Nível de prioridade do efeito a ser recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor HRESULT. Os possíveis valores incluem os seguintes:



| Código de retorno                                                                               | Descrição                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>   | Sem efeito na prioridade especificada,<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito.<br/>                             |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo** .<br/>           |



 

## <a name="remarks"></a>Comentários

Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> para obter o Qedit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineEffectable**](iamtimelineeffectable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




