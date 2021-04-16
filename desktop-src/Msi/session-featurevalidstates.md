---
description: A propriedade FeatureValidStates do objeto Session retorna um inteiro que representa os sinalizadores de bit com cada bit relevante que representa um estado de instalação válido para o recurso especificado.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Propriedade Session. FeatureValidStates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751422"
---
# <a name="sessionfeaturevalidstates-property"></a>Propriedade Session. FeatureValidStates

A propriedade **FeatureValidStates** do objeto [**Session**](session-object.md) retorna um inteiro que representa os sinalizadores de bit com cada bit relevante que representa um estado de instalação válido para o recurso especificado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a>Valor da propriedade

Nome de cadeia de caracteres necessário do item de recurso cujos Estados de instalação válidos devem ser recuperados.

## <a name="remarks"></a>Comentários

O valor de retorno é composto de sinalizadores de bit da seguinte maneira. Bit 0: se definido, local é um estado válido. Bit 1: se definido, a origem será um estado válido.

A propriedade **FeatureValidStates** só terá sucesso depois que o instalador tiver chamado as ações [CostInitialize](costinitialize-action.md) e [CostFinalize](costfinalize-action.md) .

**FeatureValidStates** determina a validade do estado consultando todos os componentes vinculados ao recurso especificado sem levar em conta o estado atual instalado de qualquer componente.

Os Estados válidos possíveis para um recurso são determinados da seguinte maneira:

-   Se o recurso não contiver componentes, a origem INSTALLstate \_ local e InstallState \_ serão Estados válidos para o recurso.
-   Se pelo menos um componente do recurso tiver um atributo de msidbComponentAttributesLocalOnly ou msidbComponentAttributesOptional, INSTALLstate \_ local será um estado válido para o recurso.
-   Se pelo menos um componente do recurso tiver um atributo de msidbComponentAttributesSourceOnly ou msidbComponentAttributesOptional, a origem INSTALLstate \_ será um estado válido para o recurso.
-   Se um arquivo de um componente pertencente ao recurso for corrigido ou de uma fonte compactada, a origem INSTALLstate \_ não será incluída como um estado válido para o recurso.
-   \_A notificação InstallState não será um estado válido se o recurso não permitir anúncio (msidbFeatureAttributesDisallowAdvertise) ou o recurso exigir o suporte de plataforma para anúncio (msidbFeatureAttributesNoUnsupportedAdvertise) e a plataforma não oferecer suporte a ela.
-   INSTALLstate \_ ausente é um estado válido para o recurso se seus atributos não incluírem msidbFeatureAttributesUIDisallowAbsent.
-   Os Estados válidos para recursos filho marcados para seguir o recurso pai (msidbFeatureAttributesFollowParent) são baseados na ação do recurso pai ou no estado instalado.

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




