---
description: Vários factoids descrevem a entrada que é comum a todos os reconhecedores de linguagem e não precisa ter formatos diferentes para idiomas diferentes. A tabela a seguir lista factoids que são comuns em todos os idiomas.
ms.assetid: dae4a28d-0332-4bb2-b040-13a959c7945e
title: Factoids comuns entre linguagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 407a82c72367d0123414f72b083b1d3416cfc958
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473872"
---
# <a name="factoids-common-across-languages"></a>Factoids comuns entre linguagens

Vários factoids descrevem a entrada que é comum a todos os reconhecedores de linguagem e não precisa ter formatos diferentes para idiomas diferentes. A tabela a seguir lista factoids que são comuns em todos os idiomas.




| Factoid | Definição | Exemplos | 
|---------|------------|----------|
| <strong>Dígito</strong> | Define o desvio para um único dígito. O reconhecedor é tendência para retornar apenas dígitos únicos quando esse factoid é definido.<br /> | 0-9<br /> | 
| <strong>Email</strong> | Define desvio para um endereço de email.<br /> | someone@example.com<br /> | 
| <strong>Web</strong> | Define o desvio para vários formatos de URL.<br /><blockquote>[!Note]<br />As configurações padrão para o reconhecedor incluem o factoid da <strong>Web.</strong> Por isso, talvez você não observe uma grande diferença entre o factoid <strong>da Web</strong> e a configuração padrão. No entanto, o factoid <strong>da Web</strong> ajuda a eliminar espaços entre palavras em uma URL.</blockquote><br /> | http: \\ microsoft.net<br /> https://microsoft.us/<br /> https: \\ www.microsoft.au \<br />https://microsoft.com<br /> www.microsoft_world.com<br /> www.microsoft.us \<br /> http: \\www.microsoft.com\myfile.htm<br /> http: \\www.microsoft.com\myfile.html<br /> http: \\ www.microsoft.com\myfile.asp<br /> http: \\ www.microsoft.uk<br /> http: \\ www.microsoft.info<br /> www.microsoft.biz<br /> | 
| <strong>Padrão</strong> | Retorna o reconhecedor para suas configurações padrão.<br /> | A configuração padrão para factoids para idiomas do oeste inclui o dicionário do sistema, <strong></strong> o dicionário de usuário, várias pontuações e os factoids <strong>Web</strong> e Number.<br /> A configuração padrão para factoids para idiomas do Leste da Ásia inclui todos os caracteres com suporte pelo reconhecedor.<br /> | 
| <strong>Nenhum</strong> | Desabilita todos os factoids, dicionários e o modelo de linguagem.<br /> | Esse factoid deve ser usado somente quando você não quiser que o reconhecedor use regras de gramática ou dicionários, incluindo o dicionário do sistema. Esse factoid é útil para a entrada de cadeias de caracteres aleatórias, como códigos de produto. Não use o sinalizador Coerce com esse factoid.<br /> | 




 

 

 




