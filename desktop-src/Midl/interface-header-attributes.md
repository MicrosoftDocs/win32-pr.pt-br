---
title: Atributos de header de interface
description: Incorpore esses atributos no header da interface para transmitir informações sobre toda a interface.
ms.assetid: 5e30c902-1a55-4afd-afba-93fcc9e75033
keywords:
- IDL MIDL, atributos, header de interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a26dac473c95625162e6dbb689f54833a166b1c58ae478654c52fededf3dd529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642982"
---
# <a name="interface-header-attributes"></a>Atributos de header de interface

Incorpore esses atributos no header da interface para transmitir informações sobre toda a interface.



| Atributo                                   | Uso                                                                                                                                                                                                                                            |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**async \_ uuid**](async-uuid.md)           | Direciona o compilador MIDL para definir versões síncronas e assíncronas de uma interface COM.                                                                                                                                               |
| [**Uuid**](uuid.md)                        | Designa um valor de 128 bits que distingue uma interface específica de todas as outras. O valor real pode representar um GUID, um CLSID ou um IID.                                                                                                 |
| [**Local**](local.md)                      | Direciona o compilador MIDL para gerar somente arquivos de header. Uma interface deve ter um [**uuid**](uuid.md) ou um [**atributo**](local.md) local.                                                                                             |
| [**ms \_ union**](-ms-union.md)              | Controla o alinhamento de NDR de uniões não truncadas. Use para compatibilidade com backward com interfaces criadas no MIDL 1.0 ou 2.0.                                                                                                                   |
| [**Objeto**](object.md)                    | Identifica a interface como uma interface COM e direciona o compilador MIDL para gerar código proxy/stub em vez de stubs de cliente e servidor RPC.                                                                                                    |
| [**Versão**](version.md)                  | Identifica uma versão específica de uma interface em casos em que existem várias versões da interface. Como as interfaces COM são imutáveis, você não pode usar o atributo [**de versão**](version.md) em uma interface [**de**](object.md) objeto. |
| [**padrão \_ do ponteiro**](pointer-default.md) | Especifica o tipo de ponteiro padrão para todos os ponteiros, exceto aqueles incluídos em listas de parâmetros. O tipo padrão pode ser [**exclusivo,**](unique.md) [**ref**](ref.md)ou [**ptr.**](ptr.md)                                                   |
| [**Extremidade**](endpoint.md)                | Especifica um ponto de extremidade estático (conhecido) no qual um aplicativo de servidor escutará chamadas de procedimento remoto.                                                                                                                                   |



 

Consulte [Atributos de biblioteca de](type-library-attributes.md) tipos para atributos de interface, como [**dual**](dual.md) e [**oleautomation**](oleautomation.md), que são específicos para interfaces definidas ou referenciadas dentro de uma instrução de biblioteca.

 

 




