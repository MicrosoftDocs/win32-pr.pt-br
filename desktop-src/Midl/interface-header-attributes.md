---
title: Atributos de cabeçalho de interface
description: Incorpore esses atributos no cabeçalho da interface para transmitir informações sobre a interface inteira.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- MIDL, atributos, cabeçalho de interface IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26dac473c95625162e6dbb689f54833a166b1c58ae478654c52fededf3dd529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642982"
---
# <a name="interface-header-attributes"></a>Atributos de cabeçalho de interface

Incorpore esses atributos no cabeçalho da interface para transmitir informações sobre a interface inteira.



| Atributo                                   | Uso                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_UUID assíncrono**](async-uuid.md)           | Direciona o compilador MIDL para definir as versões síncrona e assíncrona de uma interface COM.                                                                                                                                               |
| [**personalizado**](uuid.md)                        | Designa um valor de 128 bits que distingue uma interface específica de todas as outras. O valor real pode representar um GUID, um CLSID ou um IID.                                                                                                 |
| [**local**](local.md)                      | Direciona o compilador MIDL para gerar somente arquivos de cabeçalho. Uma interface deve ter um [**UUID**](uuid.md) ou um atributo [**local**](local.md) .                                                                                             |
| [**\_União MS**](-ms-union.md)              | Controla o alinhamento de NDR de uniões não encapsuladas. Use para compatibilidade com versões anteriores com interfaces criadas no MIDL 1,0 ou 2,0.                                                                                                                   |
| [**objeto**](object.md)                    | Identifica a interface como uma interface COM e direciona o compilador MIDL para gerar código de proxy/stub em vez de stubs de cliente e de servidor RPC.                                                                                                    |
| [**Versão**](version.md)                  | Identifica uma versão específica de uma interface em casos em que existem várias versões da interface. Como as interfaces COM são imutáveis, você não pode usar o atributo [**version**](version.md) em uma interface de [**objeto**](object.md) . |
| [**padrão de ponteiro \_**](pointer-default.md) | Especifica o tipo de ponteiro padrão para todos os ponteiros, exceto aqueles incluídos nas listas de parâmetros. O tipo padrão pode ser [**Unique**](unique.md), [**ref**](ref.md)ou [**PTR**](ptr.md).                                                   |
| [**extremidade**](endpoint.md)                | Especifica um ponto de extremidade estático (bem conhecido) no qual um aplicativo de servidor escutará chamadas de procedimento remotas.                                                                                                                                   |



 

Consulte [atributos de biblioteca de tipos](type-library-attributes.md) para atributos de interface, como [**Dual**](dual.md) e [**oleautomation**](oleautomation.md), que são específicos para interfaces definidas ou referenciadas dentro de uma instrução de biblioteca.

 

 




