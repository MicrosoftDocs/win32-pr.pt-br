---
description: ICE82 valida que a ação RegisterProduct, a ação RegisterUser, a ação PublishProduct e a ação PublishFeatures estão presentes na tabela InstallExecuteSequence. O pacote será validado se todas as ações estiverem presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf620bd58ca59315796941c6e8d9d3e4c12cdca9064d2be79058c89201a91bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105226"
---
# <a name="ice82"></a>ICE82

ICE82 valida que a ação [RegisterProduct](registerproduct-action.md), a ação [RegisterUser](registeruser-action.md), a [ação PublishProduct](publishproduct-action.md)e a [ação PublishFeatures](publishfeatures-action.md) estão presentes na [tabela InstallExecuteSequence](installexecutesequence-table.md). O pacote será validado se todas as ações estiverem presentes.

ICE82 posta um aviso se houver duas ações com o mesmo número de sequência listado nas tabelas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence.

## <a name="result"></a>Resultado

ICE82 posta os seguintes avisos.



| Aviso de ICE82                                                                                                                                                                                                                 | Descrição                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| A tabela InstallExecuteSequence não contém o conjunto de ações mencionadas abaixo: ações ausentes:<br/> Recursos de publicação<br/> Publicar produto<br/> Registrar produto<br/> Registrar usuário<br/> | ICE82 ação personalizada postará um aviso se todas as quatro ações estiverem ausentes.                                                                                                                                         |
| Esta ação \[ 1 \] tem o número de sequência duplicado \[ 2 \] na tabela \[ 3 \] .                                                                                                                                                     | ICE82 posta um aviso se houver duas ações com o mesmo número de sequência listado nas tabelas InstallExecuteSequence, InstallUISequence, AdminExecuteSequence, AdminUISequence ou AdvtExecuteSequence. |



 

ICE82 posta os erros a seguir.



| Erro de ICE82                                                                                                                                                                                                                                        | Descrição                                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| O InstallExecuteSequence deve conter todas as ações mencionadas abaixo ou nenhuma dessas ações presentes<br/> <List of actions present> <br/> Ações ausentes:<br/> <List of actions missing> <br/> | ICE82 lançará um erro se algumas das quatro ações estiverem presentes e outras estiverem ausentes. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 




