---
title: o MSAA não está disponível para Windows aplicativos da loja
description: o MSAA não está disponível para Windows aplicativos da loja
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabfd0f855cc4d3940a68fd18e69c4ca2a93774ccdbd0fb1868d2f8f489abea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935076"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>o MSAA não está disponível para Windows aplicativos da loja

## <a name="platform"></a>Plataforma

**clientes** – Windows 8 


## <a name="description"></a>Descrição

Windows 8 não dá suporte a MSAA (Microsoft Acessibilidade Ativa) para ler ou automatizar dados acessíveis de aplicativos da loja Windows. a API de automação da interface do usuário (UIA), disponível desde Windows 7, deve ser usada em seu lugar. como não há nenhum recurso de aplicativo da Windows Store existente, não há nenhuma implementação existente afetada por essa alteração. Isso afeta apenas os novos aplicativos e recursos escritos para Windows 8. Os desenvolvedores ainda podem usar a MSAA para expor seus dados de acessibilidade. se os dados MSAA forem fornecidos pelo provedor de aplicativo Windows Store, os clientes UIA ainda poderão ler e automatizar os dados.

para simplificar a API para Windows aplicativos da loja 8Windows, decidimos dar suporte apenas à automação da interface do usuário como um cliente para esses aplicativos. Os clientes UIA podem ler provedores UIA nativamente, sem tradução. Os clientes UIA podem ler provedores de MSAA como convertidos por meio do proxy UIA-to-MSAA. isso reduzirá a carga de teste para os desenvolvedores de aplicativos da loja Windows.

A eliminação do suporte para provedores de MSAA reduziria ainda mais a matriz de testes, mas há aplicativos principais que ainda são baseados em MSAA e não queremos renderizá-los inacessíveis.

## <a name="manifestation"></a>Manifestação

Windows Os desenvolvedores de aplicativos da Store não poderão acessar os detalhes do MSAA no modelo de aplicativo.

## <a name="solution"></a>Solução

nenhum novo caso automatizado deve ser criado no MSAA para recursos de aplicativos da Windows Store.

alterne qualquer ferramenta interna existente que use MSAA para UIA se precisar interagir com Windows aplicativos da loja. Windows Os desenvolvedores de aplicativos da loja devem usar a API de automação da interface do usuário.

## <a name="resources"></a>Recursos

-   [Conceitos básicos de automação da interface do usuário](../winauto/entry-uiauto-win32.md)

 

 