---
description: Saiba como dar suporte a diferentes versões da estrutura de esquema de impressão. Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: fc89dd2d-9a5d-400b-aee9-a1e4cf7d83da
title: Suporte a versões de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac627d3dd711bc952d881efd393720af128e7f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120591"
---
# <a name="supporting-schema-versions"></a>Suporte a versões de esquema

Este tópico não é atual. Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

A estrutura do esquema de impressão está sujeita a alterações no futuro conforme surgem as novas necessidades. Essas alterações devem ser muito frequentes, pois a alteração mais comum é a introdução de novos nomes de instância. Essa alteração não afeta a estrutura da estrutura e deve ser transparente para clientes e provedores. Quaisquer alterações na estrutura e na organização da estrutura de esquema de impressão serão identificadas por incrementos para seu número de versão. As inclusões nas palavras-chave do esquema de impressão não serão identificadas. Os provedores PrintTicket devem ser capazes de dar suporte à versão atual da estrutura de esquema de impressão, bem como a qualquer versão anterior. A versão da estrutura de esquema de impressão é identificada usando o atributo XML: versão que aparece no elemento raiz do PrintTicket.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Especificação de esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



