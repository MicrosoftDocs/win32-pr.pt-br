---
title: Considerações sobre mercados internacionais
description: Considerações sobre mercados internacionais
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player online, mercados internacionais
- lojas online, mercados internacionais
- tipo 1 lojas online, mercados internacionais
- tipo 2 lojas online, mercados internacionais
- mercados internacionais
- Windows Media Player online, documento ServiceInfo
- lojas online, documento ServiceInfo
- type 1 online stores,ServiceInfo document
- type 2 online stores,ServiceInfo document
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e2db056f748e1257649716c57a2f1774ee0b1b149966dce3851a75d08c8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580506"
---
# <a name="considerations-for-international-markets"></a>Considerações sobre mercados internacionais

Se sua empresa criar lojas online para vários mercados, você deverá fornecer à Microsoft a URL de um documento ServiceInfo para cada mercado. Você pode fazer isso de duas maneiras a seguir:

-   Crie um documento ServiceInfo separado para cada mercado. Nesse caso, você fornece à Microsoft URLs que apontam para documentos serviceInfo individuais para cada loja online em cada mercado.
-   Crie um único documento ServiceInfo para todos os mercados. Ao fazer isso, você fornece à Microsoft a mesma URL para cada mercado. O documento ServiceInfo, criado como uma página ASP, pode detectar dinamicamente o local do usuário com base nos parâmetros da cadeia de caracteres de consulta.

Windows Media Player anexa uma cadeia de consulta à solicitação de URL do ServiceInfo que fornece informações sobre as configurações de localidade e local do usuário. Se sua loja online usar essas informações para determinar qual conteúdo exibir, você deverá anexar dinamicamente esses valores às suas próprias URLs no documento ServiceInfo. Essa é a melhor maneira de garantir que suas URLs de página da Web sempre conterão os parâmetros esperados.

Depois de determinar o local e a preferência de idioma do usuário, talvez você queira persistir essas informações para sessões futuras. Você pode fazer isso usando qualquer uma das técnicas que normalmente usaria em uma página da Web, como cookies ou usando seu objeto COM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando o documento ServiceInfo dinamicamente**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Informações comuns às lojas online do tipo 1 e do tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Elemento ServiceInfo**](serviceinfo-element.md)
</dt> </dl>

 

 




