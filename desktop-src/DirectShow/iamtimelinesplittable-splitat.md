---
description: O método SplitAt divide o objeto na hora especificada.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Método IAMTimelineSplittable:: SplitAt (QEdit. h)'
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
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784025"
---
# <a name="iamtimelinesplittablesplitat-method"></a>Método IAMTimelineSplittable:: SplitAt

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `SplitAt` método divide o objeto na hora especificada.

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

Hora na qual dividir o objeto, em relação ao início da linha do tempo, em unidades de 100 nanossegundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                   | Descrição                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>       | Nada para dividir.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Êxito.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | O objeto não existe no momento.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memória insuficiente.<br/>                    |



 

## <a name="remarks"></a>Comentários

Se você dividir uma origem, um efeito ou uma transição, esse método criará um segundo objeto do mesmo tipo. O objeto original é truncado no tempo de divisão especificado e o novo objeto substitui a parte truncada. O novo objeto herda todas as mesmas propriedades. Em um objeto de origem, o método também divide todos os efeitos que se enquadram no tempo de divisão.

Chamar esse método em uma faixa divide todas as origens, efeitos e transições que estão contidos na faixa no tempo de divisão especificado. Ele não cria uma segunda faixa. (Uma faixa começa no tempo zero e se estende ao infinito.)

Para uma faixa, se o tempo de divisão for posterior ao que tudo na faixa, o método retornará S \_ false. Para qualquer outro objeto, se o tempo de divisão não cair em nenhum lugar dentro do objeto, o método retornará E \_ INVALIDARG.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IAMTimelineSplittable**](iamtimelinesplittable.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




