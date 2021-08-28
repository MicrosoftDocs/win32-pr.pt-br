---
description: O &\# 0034; O campo \# de bits&0034; tipo sem solicitações de contexto que o usuário fornece um inteiro cujo valor é usado para definir um ou mais bits em um campo de conteúdo. Esse texto pode estar em qualquer idioma compatível com a página de código do banco de dados.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo de campo de bits arbitrário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521889ffb1677bed249a92f757556a2fdbe36768
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884573"
---
# <a name="arbitrary-bitfield-type"></a>Tipo de campo de bits arbitrário

O tipo "campo de teletexto" sem solicitações de contexto que o usuário fornece um inteiro cujo valor é usado para definir um ou mais bits em um teletipo. Esse texto pode estar em qualquer idioma compatível com a página de código do banco de dados.

O tipo de linguagem de bits arbitrária do [tipo semântico](semantic-types.md) é um dos tipos de campo de bits. Esse tipo consiste em um inteiro escolhido pelo usuário de um conjunto de opções. A ferramenta de mesclagem substitui o inteiro selecionado nos modelos especificados na coluna valor da [tabela ModuleSubstitution](modulesubstitution-table.md). Para especificar um item configurável desse tipo, os autores de módulo devem inserir o nome do item na coluna nome, inserir "3" na coluna formato, deixar a coluna tipo em branco e inserir a lista de inteiros possíveis na coluna ContextData da [Tabela ModuleConfiguration](moduleconfiguration-table.md).

A coluna de tipo é reservada e deve ser nula. A entrada na coluna ContextData para todos os tipos de formato de campo de bits deve estar no formato " &lt; Mask &gt; ; &lt; Valor do nome &gt; = &lt; &gt; ; &lt; Nome &gt; = &lt; valor &gt; .... ", em que &lt; Mask &gt; é um valor inteiro que indica os bits de interesse, &lt; name &gt; é um nome de exibição localizável para a escolha, e &lt; Value &gt; é um valor inteiro decimal. A coluna de contexto está em usar o [formato especial CMSM](cmsm-special-format.md) e para todos os tipos de campo de bits. Um caractere literal "=" ou ";" pode ser inserido no &lt; campo nome &gt; , prefixando-o com um caractere de barra invertida (' \\ ').

 

 



