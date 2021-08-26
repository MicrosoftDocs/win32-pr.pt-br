---
title: Sintaxe do grupo de efeitos (Direct3D 11)
description: Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1b2c72b0a67a31911a0f2c9f9ae6ac0e9e20463a850c303dab4a208401d1c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069746"
---
# <a name="effect-group-syntax-direct3d-11"></a>Sintaxe do grupo de efeitos (Direct3D 11)

Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.


```
fxgroup GroupName  [ <Annotations > ]
{
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
    TechniqueVersion TechniqueName [ <Annotations > ] 
    { 
       ...
    } 
}



```



## <a name="parameters"></a>Parâmetros



| Item                                                                                                                                                                           | Descrição                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | palavra-chave equired.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>Groupname<br/>                                                                       | Obrigatórios. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome do grupo de efeitos. Ao contrário das técnicas, os grupos devem ter nomes para garantir que as técnicas tenham um identificador exclusivo (consulte a seção Grupos e Técnicas abaixo).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < anotações ><br/> | \[em \] Opcional. Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para sintaxe, consulte Sintaxe de anotação (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | "technique10" ou "technique11". As técnicas que usam a funcionalidade nova para o Direct3D 11 (sombreadores \_ 5 0, BindInterfaces, etc.) devem usar "technique11".<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>TechniqueName<br/>                                                       | Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Grupos e técnicas

Para manter a compatibilidade com efeitos fx \_ 4 \_ 0, os grupos são opcionais. Há um grupo nomeado null implícito em torno de todas as técnicas globais.

Considere o seguinte exemplo:


```
technique11 GlobalTech
{
}
fxgroup Group1
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
fxgroup Group2
{
     technique11 Tech1 { ... }
     technique11 Tech2 { ... }
}
```



No C++, é possível obter uma técnica por nome de duas maneiras. Os comandos a seguir encontrarão as técnicas óbvias:


```
pEffect->GetTechniqueByName( "GlobalTech" );
pEffect->GetTechniqueByName( "|GlobalTech" );
pEffect->GetTechniqueByName( "Group1|Tech1" );
pEffect->GetTechniqueByName( "Group1|Tech2" );
pEffect->GetTechniqueByName( "Group2|Tech1" );
pEffect->GetTechniqueByName( "Group2|Tech2" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group1")->GetTechniqueByName( "Tech2" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech1" );
pEffect->GetGroupByName("Group2")->GetTechniqueByName( "Tech2" );
```



Para garantir que [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funcione de forma semelhante aos Efeitos 10, todos os grupos definidos devem ter um nome.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de efeito](d3d11-effect-format.md)
</dt> <dt>

[Sintaxe da técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





