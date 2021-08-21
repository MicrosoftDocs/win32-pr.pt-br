---
title: Evento de indicador
description: Evento de indicador
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976705"
---
# <a name="bookmark-event"></a>Evento de indicador

\[O Microsoft Agent foi preterido a partir Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Ocorre quando um indicador em uma cadeia de caracteres de texto de fala que seu aplicativo definiu é ativado.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**
</dt> <dd>

**Indicador** *do* \_ **sub-agente** **(ByVal** *BookmarkID***)**



| Parte         | Descrição                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | Um inteiro longo que identifica o número do indicador. |



 

</dd> </dl>

### <a name="remarks"></a>Comentários

Para especificar um evento de indicador, use [**o método Speak**](speak-method.md) com uma marca **Mrk** no texto fornecido. Para obter mais informações sobre marcas, consulte Marcas de saída de fala.

 

 




