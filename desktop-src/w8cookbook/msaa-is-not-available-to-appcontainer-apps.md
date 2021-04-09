---
title: A MSAA não está disponível para aplicativos da Windows Store
description: A MSAA não está disponível para aplicativos da Windows Store
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008501"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a>A MSAA não está disponível para aplicativos da Windows Store

## <a name="platform"></a>Plataforma

**Clientes** – Windows 8 


## <a name="description"></a>Descrição

O Windows 8 não oferece suporte a MSAA (Microsoft Acessibilidade Ativa) para ler ou automatizar dados acessíveis de aplicativos da Windows Store. A API de automação da interface do usuário (UIA), disponível desde o Windows 7, deve ser usada em seu lugar. Como não há nenhum recurso existente do aplicativo da Windows Store, não há nenhuma implementação existente afetada por essa alteração. Isso afeta apenas os novos aplicativos e recursos escritos para o Windows 8. Os desenvolvedores ainda podem usar a MSAA para expor seus dados de acessibilidade. Se os dados MSAA forem fornecidos pelo provedor de aplicativos da Windows Store, os clientes UIA ainda poderão ler e automatizar os dados.

Para simplificar a API para aplicativos da Windows 8Windows Store, decidimos dar suporte apenas à automação da interface do usuário como um cliente para esses aplicativos. Os clientes UIA podem ler provedores UIA nativamente, sem tradução. Os clientes UIA podem ler provedores de MSAA como convertidos por meio do proxy UIA-to-MSAA. Isso reduzirá a carga de teste para os desenvolvedores de aplicativos da Windows Store.

A eliminação do suporte para provedores de MSAA reduziria ainda mais a matriz de testes, mas há aplicativos principais que ainda são baseados em MSAA e não queremos renderizá-los inacessíveis.

## <a name="manifestation"></a>Manifestação

Os desenvolvedores de aplicativos da Windows Store não poderão acessar os detalhes do MSAA no modelo de aplicativo.

## <a name="solution"></a>Solução

Nenhum novo caso automatizado deve ser criado no MSAA para recursos dos aplicativos da Windows Store.

Alterne qualquer ferramenta interna existente que use MSAA para UIA se precisar interagir com aplicativos da Windows Store. Os desenvolvedores de aplicativos da Windows Store devem usar a API de automação da interface do usuário.

## <a name="resources"></a>Recursos

-   [Conceitos básicos de automação da interface do usuário](../winauto/entry-uiauto-win32.md)

 

 