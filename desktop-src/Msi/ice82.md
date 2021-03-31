---
description: ICE82 valida que a ação RegisterProduct, a ação RegisterUser, a ação PublishProduct e a ação PublishFeatures estão presentes na tabela InstallExecuteSequence. O pacote será validado se todas as ações estiverem presentes.
ms.assetid: b41a56f9-b57e-4133-ae7d-c51b36bab44f
title: ICE82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa6ba2e0bd07af06bf90c604c333966b5581ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662793"
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

 

 




