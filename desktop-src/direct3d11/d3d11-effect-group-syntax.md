---
title: Sintaxe do grupo de efeitos (Direct3D 11)
description: Um grupo de efeitos é declarado com a sintaxe descrita nesta seção.
ms.assetid: f6695ae5-198f-45bd-853b-8c02fabd0c39
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9221341810990801f1ed07005e0dcb917df42360
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104453797"
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
| <span id="fxgroup"></span><span id="FXGROUP"></span>fxgroup<br/>                                                                                                         | palavra-chave ecessário.<br/>                                                                                                                                                                                                         |
| <span id="GroupName"></span><span id="groupname"></span><span id="GROUPNAME"></span>GroupName<br/>                                                                       | Obrigatórios. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome do grupo de efeitos. Ao contrário das técnicas, os grupos devem ter nomes para garantir que as técnicas tenham um identificador exclusivo (consulte a seção grupos e técnicas abaixo).<br/> |
| <span id="_______________Annotations__"></span><span id="_______________annotations__"></span><span id="_______________ANNOTATIONS__"></span> < anotações ><br/> | \[em \] opcional. Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito. Para obter a sintaxe, consulte Sintaxe de anotação (Direct3D 11). <br/>                                                      |
| <span id="TechniqueVersion"></span><span id="techniqueversion"></span><span id="TECHNIQUEVERSION"></span>TechniqueVersion<br/>                                           | "Technique10" ou "technique11". As técnicas que usam a funcionalidade nova para o Direct3D 11 (5 \_ 0 shaders, BindInterfaces, etc.) devem usar "technique11".<br/>                                                                 |
| <span id="TechniqueName"></span><span id="techniquename"></span><span id="TECHNIQUENAME"></span>Técnicaname<br/>                                                       | Opcional. Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da técnica de efeito. <br/>                                                                                                                                    |



 

## <a name="groups-and-techniques"></a>Grupos e técnicas

Para manter a compatibilidade com efeitos FX \_ 4 \_ 0, os grupos são opcionais. Há um grupo com nome nulo implícito em torno de todas as técnicas globais.

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



Em C++, é possível obter uma técnica por nome de duas maneiras. Os seguintes comandos encontrarão as técnicas óbvias:


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



Para garantir que [**ID3DX11Effect:: GetTechniqueByName**](id3dx11effect-gettechniquebyname.md) funcione da mesma forma que os efeitos 10, todos os grupos definidos devem ter um nome.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](d3d11-effect-format.md)
</dt> <dt>

[Sintaxe da técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md)
</dt> </dl>

 

 





