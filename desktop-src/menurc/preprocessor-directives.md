---
title: Diretivas de pré-processador (menus e outros recursos)
description: Você pode usar as diretivas descritas na tabela a seguir, conforme necessário no script de recurso. Eles instruem o RC para executar ações ou para atribuir valores a nomes.
ms.assetid: 162f946e-54d8-4e23-9aa7-8e91eda4ee68
keywords:
- compilador de recurso, diretivas de pré-processador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43e8c32f1d32dab784d5d947fdf64b7018451a5a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104294732"
---
# <a name="preprocessor-directives-menus-and-other-resources"></a>Diretivas de pré-processador (menus e outros recursos)

Você pode usar as diretivas descritas na tabela a seguir, conforme necessário no script de recurso. Eles instruem o RC para executar ações ou para atribuir valores a nomes.



| Diretiva                     | Descrição                                                           |
|-------------------------------|-----------------------------------------------------------------------|
| [**\#definir**](-define.md)   | Define um nome especificado atribuindo a ele um determinado valor.               |
| [**\#elif**](-elif.md)       | Marca uma cláusula opcional de um bloco de compilação condicional.          |
| [**\#else**](-else.md)       | Marca a última cláusula opcional de um bloco de compilação condicional.    |
| [**\#endif**](-endif.md)     | Marca o final de um bloco de compilação condicional.                     |
| [**\#que**](-if.md)           | Compila condicionalmente o script se uma expressão especificada for verdadeira.  |
| [**\#ifdef**](-ifdef.md)     | Compila condicionalmente o script se um nome especificado for definido.     |
| [**\#ifndef**](-ifndef.md)   | Compila condicionalmente o script se um nome especificado não estiver definido. |
| [**\#incluir**](-include.md) | Copia o conteúdo de um arquivo para o arquivo de definição de recurso.      |
| [**\#undef**](-undef.md)     | Remove a definição do nome especificado.                         |



 

Para definir símbolos para seus identificadores de recursos, use a diretiva **\# definir** para defini-los em um arquivo de cabeçalho. Inclua esse cabeçalho no script de recurso e no código-fonte do aplicativo. Da mesma forma, você define os valores para atributos de recurso e estilos, incluindo o Windows. h no script de recurso.

O RC trata os arquivos com as extensões. c e. h de maneira especial. Ele pressupõe que um arquivo com uma dessas extensões não contém recursos. Se um arquivo tiver a extensão de nome de arquivo. c ou. h, o RC ignorará todas as linhas no arquivo, exceto as diretivas de pré-processador. Portanto, para incluir um arquivo que contém recursos em outro script de recurso, dê ao arquivo uma extensão diferente de. c ou. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Diretivas pragma](pragma-directives.md)
</dt> </dl>

 

 




