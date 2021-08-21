---
title: Interfaces ADSI
description: Este tópico descreve as categorias usadas para interfaces ADSI.
ms.assetid: 8c735dbf-41d7-4fbb-b372-9abe4e1b8fdd
ms.tgt_platform: multiple
keywords:
- ADSI de interfaces ADSI
- ADSI da ADSI, referência, interfaces
- ADSI de interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75463a2b9ce70013482d2abee4f21ff786e7914cff0fefe691c562c4f39edb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023814"
---
# <a name="adsi-interfaces"></a>Interfaces ADSI

A ADSI (Active Directory Service Interfaces) dá suporte a um conjunto avançado de interfaces que podem ser classificadas de acordo com as seguintes categorias:

-   [Núcleo](core-interfaces.md). Essas interfaces fornecem as funções básicas de gerenciamento de objeto dos objetos ADSI. As funções principais incluem o fornecimento de um ponto de entrada em um repositório de diretório, o carregamento de propriedades no cache de propriedades e a confirmação de alterações no diretório subjacente.
-   [Esquema](schema-interfaces.md). Essas interfaces fornecem métodos para gerenciar e estender o esquema de diretório.
-   [Cache de propriedades](property-cache-interfaces.md). Essas interfaces definem métodos para manipular propriedades no cache de propriedades.
-   [Objeto persistente](persistent-object-interfaces.md). Essas interfaces manipulam dados persistentes no namespace do serviço de diretório subjacente. Os objetos ADSI implementam esses tipos de interfaces para fornecer acesso aos seus dados persistentes, incluindo contas de usuário, compartilhamentos de arquivos, hierarquias organizacionais e listagens de trabalhos em uma fila de impressão.
-   [Objeto dinâmico](dynamic-object-interfaces.md). Essas interfaces funcionam com dados dinâmicos em um serviço de diretório. Os objetos de diretório não representados no serviço de diretório subjacente implementam essas interfaces. Exemplos de dados dinâmicos incluem comandos emitidos por uma rede.
-   [Segurança](security-interfaces.md). Essas interfaces permitem que um cliente ADSI estabeleça suas credenciais para um servidor e use recursos de segurança aos quais o serviço de diretório dá suporte, como a lista de controle de acesso ou descritores de segurança.
-   [Não automação](non-automation-interfaces.md). Essas interfaces permitem que clientes que não são de automação (por exemplo, aplicativos C/C++) tenham acesso de baixa sobrecarga a objetos de diretório, fornecendo acesso de vtable a métodos para gerenciar e Pesquisar objetos de serviço de diretório.
-   [Extensão](extension-interfaces.md). Essas interfaces permitem que os clientes ADSI estendam os recursos das classes ADSI existentes para oferecer soluções personalizadas aos serviços de diretório.
-   [Utilitário](utility-interfaces.md). Essas interfaces fornecem funções auxiliares avançadas para o gerenciamento de objetos ADSI.
-   [Tipo de dados](data-type-interfaces.md). Essas interfaces fornecem métodos para acessar tipos de dados ADSI.

 

 




