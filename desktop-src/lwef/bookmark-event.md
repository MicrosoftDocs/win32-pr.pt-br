---
title: Evento de indicador
description: Evento de indicador
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159651"
---
# <a name="bookmark-event"></a>Evento de indicador

\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**
</dt> <dd>

Ocorre quando um indicador em uma cadeia de caracteres de texto de fala que seu aplicativo definiu é ativado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

 Indicador de *subagente* \_  **(ByVal** *BookmarkID * * *)**



| Parte         | Descrição                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Um inteiro longo que identifica o número do indicador. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Para especificar um evento de indicador, use o método [**Speak**](speak-method.md) com uma marca **mrk** no texto fornecido. Para obter mais informações sobre marcas, consulte marcas de saída de fala.

 

 




