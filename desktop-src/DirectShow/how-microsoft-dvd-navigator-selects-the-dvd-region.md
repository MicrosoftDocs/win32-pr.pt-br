---
description: Como o navegador de DVD da Microsoft seleciona a região do DVD
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Como o navegador de DVD da Microsoft seleciona a região do DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759553"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Como o navegador de DVD da Microsoft seleciona a região do DVD

O navegador de DVD da Microsoft usa o seguinte algoritmo para determinar a correspondência de região ao reproduzir discos de DVD em um PC:

1.  O navegador de DVD Obtém a região do disco, a região da unidade e a região do decodificador.
2.  Se a região do disco for "todas as regiões", o navegador de DVD reproduzirá o disco.
3.  Se o disco não estiver marcado para todas as regiões, o navegador de DVD verificará se o decodificador tem uma região predefinida.
4.  Se o decodificador tiver uma região predefinida e não corresponder à região do disco, o navegador de DVD retornará um erro indicando que ele não pode reproduzir o disco na configuração do DVD atual. Sido
5.  Se a região do decodificador não estiver definida ou for igual à região do disco, o navegador de DVD verificará se a região da unidade é igual à região do disco.
6.  Se a região da unidade corresponder à região do disco, o navegador de DVD reproduzirá o título.
7.  Caso contrário, se a região do driver não corresponder à região do disco, o navegador de DVD invocará o código para alterar a região da unidade. Se o número permitido de alterações de região tiver sido esgotado, a tentativa de alteração de região falhará e o título não poderá ser reproduzido nesse sistema.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à alteração da região do DVD no Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



