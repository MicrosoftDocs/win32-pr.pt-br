---
title: Objetos Internet-Aware
description: Objetos Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917724"
---
# <a name="internet-aware-objects"></a>Objetos Internet-Aware

Há determinadas categorias identificadas para cobrir as interfaces persistência; Elas foram identificadas como resultado da definição de como os controles funcionam pela Internet. Um contêiner que não dá suporte a todo o intervalo de interfaces persistência deve garantir que ele não hospede um controle que exija uma combinação de interfaces para as quais ele não dá suporte.

As tabelas a seguir descrevem o significado de várias categorias como categorias implementadas e obrigatórias.



| Categorias necessárias                                                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATID \_ PERSISTSTOMEMORY, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | Cada uma dessas categorias é mutuamente exclusiva e usada apenas quando um objeto dá suporte a apenas um mecanismo de persistência (portanto, a exclusão mútua). Contêineres que não dão suporte ao mecanismo de persistência descrito por uma dessas categorias devem impedir a criação de qualquer objeto de classes, portanto marcados.<br/> |
| RequiresDataPathHost de CATID \_<br/>                                                                                                                                                             | O objeto requer a capacidade de salvar dados em um ou mais caminhos e requer envolvimento de contêiner, portanto, exigindo suporte de contêiner para [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).<br/>                                                                                                                                  |



 



| Categorias implementadas                                                                                                                                                                            | Descrição                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| CATID \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATID \_ PERSISTSTOMEMORY, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag<br/> | O objeto dá suporte ao mecanismo de IPersist correspondente \* para a categoria.<br/> |



 

A tabela a seguir fornece as CATIDs exatas atribuídas a cada categoria:



| Categoria                                | CATID                                           |
|-----------------------------------------|-------------------------------------------------|
| RequiresDataPathHost de CATID \_<br/>  | 0de86a50-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToMoniker de CATID \_ <br/>    | 0de86a51-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStorage de CATID \_ <br/>    | 0de86a52-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStreamInit de CATID \_ <br/> | 0de86a53-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToStream de CATID \_ <br/>     | 0de86a54-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToMemory de CATID \_ <br/>     | 0de86a55-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToFile de CATID \_ <br/>       | 0de86a56-2baa-11cf-a229-00aa003d7352<br/> |
| PersistsToPropertyBag de CATID \_<br/> | 0de86a57-2baa-11cf-a229-00aa003d7352<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Categorias de componentes](component-categories.md)
</dt> </dl>

 

