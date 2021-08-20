---
description: Como o Navegador de DVD da Microsoft seleciona a região do DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Como o Navegador de DVD da Microsoft seleciona a região do DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a546276c57296bb4514e3ab2c8917abfe7218fe3afeadd528ac6bd80066d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999765"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Como o Navegador de DVD da Microsoft seleciona a região do DVD

O Navegador de DVD da Microsoft usa o seguinte algoritmo para determinar a corresponder à região durante a reprodução de discos de DVD em um computador:

1.  O Navegador de DVD obtém a região do disco, a região da unidade e a região do decodificador.
2.  Se a região do disco for "todas as regiões", o Navegador de DVD tocará o disco.
3.  Se o disco não estiver marcado para todas as regiões, o Navegador de DVD verificará se o decodificador tem uma região predefinida.
4.  Se o decodificador tiver uma região predefinida e não corresponder à região do disco, o Navegador de DVD retornará um erro indicando que ele não pode reproduzir o disco na configuração atual do DVD. (Sair)
5.  Se a região do decodificador não estiver definida ou for igual à região do disco, o Navegador de DVD verificará se a região da unidade é igual à região do disco.
6.  Se a região da unidade corresponde à região do disco, o Navegador de DVD reproduz o título.
7.  Caso contrário, se a região do driver não corresponder à região do disco, o Navegador de DVD invocará o código para alterar a região da unidade. Se o número permitido de alterações de região tiver sido esgotado, a tentativa de alteração de região falhará e o título não poderá ser interpretado nesse sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte para alteração de região de DVD Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



