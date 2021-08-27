---
title: Instrução switch (Urlmon.h)
description: Transfira o controle para um bloco de instrução diferente dentro do corpo da opção, dependendo do valor de um seletor.
ms.assetid: d1932ee1-d789-4536-b77d-162aacdbb115
keywords:
- Switch Statement HLSL
topic_type:
- apiref
api_name:
- switch Statement
api_location:
- urlmon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8527853bf88b073f3505f4b4170ff6165f7f9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477482"
---
# <a name="switch-statement"></a>Instrução Switch

Transfira o controle para um bloco de instrução diferente dentro do corpo da opção, dependendo do valor de um seletor.


\[*Atributo* \] switch( *Selector* ) { case 0 : { *StatementBlock*; }   break;   case 1: { *StatementBlock*; }   break;   case n : { *StatementBlock*; }   break;   default : { *StatementBlock*; }   break;



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>*Atributo*
</dt> <dd>

Um parâmetro opcional que controla como a instrução é compilada. Quando nenhum atributo é especificado, o compilador pode usar uma opção de hardware ou emitir uma série de instruções **if.**




| Atributo | Descrição | 
|-----------|-------------|
| mesclar | Compile a instrução como uma série de <strong>instruções if,</strong> cada uma com o <strong>atributo flatten.</strong> | 
| branch | Compile a instrução como uma série de <strong>instruções if</strong> cada uma com o <strong>atributo branch.</strong><blockquote>[!Note]<br />Quando você usa o Modelo de Sombreador <a href="dx-graphics-hlsl-sm2.md">2.x</a> ou o Modelo de Sombreador <a href="dx-graphics-hlsl-sm3.md">3.0</a>, sempre que usa a ramificação dinâmica, você consome recursos. Portanto, se você usar a ramificação dinâmica excessivamente ao direcionar esses perfis, poderá receber erros de compilação.</blockquote><br /> | 
| forcecase | Force uma instrução switch no hardware.<blockquote>[!Note]<br />Requer <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware de nível</a> de recurso 10_0 ou posterior.</blockquote><br /> | 
| chamada | Os corpos dos casos individuais na opção serão movidos para sub-rotinas de hardware e a opção será uma série de chamadas de sub-rotina.<blockquote>[!Note]<br />Requer <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">hardware de nível</a> de recurso 10_0 ou posterior.</blockquote><br /> | 




 

</dd> <dt>

<span id="Selector"></span><span id="selector"></span><span id="SELECTOR"></span>*Seletor*
</dt> <dd>

Uma variável. As instruções case dentro dos colchetes verificarão cada variável para ver se SwitchValue corresponde a seu CaseValue específico.

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Uma ou mais [instruções](dx-graphics-hlsl-statement-blocks.md).

</dd> </dl>

## <a name="remarks"></a>Comentários


```
[branch] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



É equivalente a:


```
[branch] if( a == 2 )
    return 3;
else if( a == 1 )
    return 1;
else if( a == 0 )
    return 0;
else
    return 6;
```



Aqui estão exemplos de usos de atributos de controle de fluxo de chamada e em letras force:


```
[forcecase] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}

[call] switch(a)
{
    case 0:
        return 0; 
    case 1:
        return 1; 
    case 2:
        return 3; 
    default:
        return 6; 
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Urlmon.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Flow Controle](dx-graphics-hlsl-flow-control.md)
</dt> </dl>

 

