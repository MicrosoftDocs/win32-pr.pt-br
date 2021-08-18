---
description: O método SplitAt divide o objeto no momento especificado.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: Método IAMTimelineSplittable::SplitAt (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cdcedc25cf7f0998c6eac11de63f6e0d329e2ca8500576e0ad9e69cfc0bb3067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052406"
---
# <a name="iamtimelinesplittablesplitat-method"></a>Método IAMTimelineSplittable::SplitAt

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SplitAt` método divide o objeto no momento especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hora* 
</dt> <dd>

Tempo no qual dividir o objeto, relativo ao início da linha do tempo, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Nada a ser dividido.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O objeto não existe no momento.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                    |



 

## <a name="remarks"></a>Comentários

Se você dividir uma origem, efeito ou transição, esse método criará um segundo objeto do mesmo tipo. O objeto original é truncado no tempo de divisão especificado e o novo objeto substitui a parte truncada. O novo objeto herda todas as mesmas propriedades. Em um objeto de origem, o método também divide os efeitos que se enquadram no tempo de divisão.

Chamar esse método em uma faixa divide todas as fontes, efeitos e transições contidas na faixa no tempo de divisão especificado. Ele não cria uma segunda faixa. (Uma faixa começa no tempo zero e se estende até o infinito.)

Para uma faixa, se o tempo de divisão for posterior a tudo na faixa, o método retornará S \_ FALSE. Para qualquer outro objeto, se o tempo de divisão não se enquadrar em nenhum lugar dentro do objeto , o método retornará E \_ INVALIDARG.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAMTimelineSplittable Interface**](iamtimelinesplittable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




