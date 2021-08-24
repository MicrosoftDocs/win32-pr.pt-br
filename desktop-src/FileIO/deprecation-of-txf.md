---
description: Este tópico discute alternativas ao uso da API NTFS Transacional (TxF) em cenários de uso comuns.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternativas ao uso de NTFS transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab924c5ee4204180b891b3aad13a5809fa07671ad0e18d6ddc9ce353122ac80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765966"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternativas ao uso de NTFS transacional

-   [Resumo](#abstract)
-   [Introdução](#introduction)
-   [Alternativas ao TxF by Scenario](#alternatives-to-txf-by-scenario)
-   [Aplicativos que atualizam um único arquivo com dados "como documento"](#applications-updating-a-single-file-with-document-like-data)
-   [Aplicativos que executam atualizações para vários arquivos e/ou para o hive do Registro](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Aplicativos que gerenciam um conjunto de dados estruturados](#applications-managing-a-set-of-structured-data)
-   [Aplicativos com transações que envolvem arquivos em um volume NTFS local e tabelas em um banco de dados SQL externo](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Fechar & ação recomendada](/windows)

## <a name="abstract"></a>Resumo

A Microsoft recomenda que os desenvolvedores investiguem utilizando as alternativas discutidas (ou, em alguns casos, investigue outras alternativas) em vez de adotar uma plataforma de API que pode não estar disponível em versões futuras do Windows.

## <a name="introduction"></a>Introdução

O TxF foi introduzido com Windows Vista como um meio de introduzir transações de arquivo atômico para Windows. Ele permite que Windows desenvolvedores tenham atomicidade transacional para operações de arquivo em transações com um único arquivo, em transações que envolvem vários arquivos e em transações que abrangem várias fontes , como o Registro (por meio de TxR) e bancos de dados (como SQL). Embora o TxF seja um conjunto poderoso de APIs, há um interesse extremamente limitado do desenvolvedor nessa plataforma de API desde o Windows Vista principalmente devido à sua complexidade e várias nuances que os desenvolvedores precisam considerar como parte do desenvolvimento de aplicativos. Como resultado, a Microsoft está pensando em preteri-lo em uma versão futura do Windows para concentrar os esforços de desenvolvimento e manutenção em outros recursos e APIs que têm mais valor para uma maioria maior de clientes. A próxima seção descreve métodos alternativos de exemplo para obter resultados semelhantes aos do TxF para vários tipos de cenários de aplicativo.

## <a name="alternatives-to-txf-by-scenario"></a>Alternativas ao TxF by Scenario

Com as limitações descritas acima, os desenvolvedores devem investigar alternativas ao TxF para abranger cenários de aplicativos que não são atendidos pelo TxF. Aqui estão algumas alternativas sugeridas para usos comuns do TxF para os desenvolvedores considerarem. Observe que essa lista não é completa nem completa.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Aplicativos que atualizam um único arquivo com dados "como documento"

Muitos aplicativos que lidam com dados "do tipo documento" tendem a carregar o documento inteiro na memória, operar nele e, em seguida, escrevê-los novamente para salvar as alterações. A atomicidade necessária aqui é que as alterações são completamente aplicadas ou não são aplicadas, pois um estado inconsistente renderizaria o arquivo corrompido. Uma abordagem comum é gravar o documento em um novo arquivo e, em seguida, substituir o arquivo original pelo novo. Um método para fazer isso é com a API [**ReplaceFile.**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Aplicativos que executam atualizações para vários arquivos e/ou para o hive do Registro

Há muitos aplicativos que precisam executar atomicamente uma atualização para um conjunto de arquivos e para o Registro. Esse cenário geralmente é obtido por meio de um aplicativo instalador, como o Windows Instalador. Para obter mais informações sobre Windows instalador, consulte [Windows Instalador do .](/windows/desktop/Msi/windows-installer-portal)

## <a name="applications-managing-a-set-of-structured-data"></a>Aplicativos que gerenciam um conjunto de dados estruturados

Muitos aplicativos gerenciam algum conjunto de estruturas de dados proprietárias de tipos variados como um meio de armazenar dados. Um desafio significativo para esses aplicativos é o processo de manter a integridade de ponteiros/referências internos se ocorrer uma falha durante uma operação de atualização. A criação do mecanismo para isso é realmente um "problema difícil" e, portanto, a maioria dos aplicativos dependerá de um servidor de banco de dados verdadeiro para gerenciar seu conjuntos de dados.

Duas sugestões para ajudar a gerenciar dados estruturados são:

-   A Microsoft fornece a caixa de entrada ESE (Extensible Armazenamento Engine) no Windows para permitir que os aplicativos executem operações de atualização e recuperação de dados transacionados. Para obter mais informações sobre o ESE (Extensible Armazenamento Engine), consulte <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Para aplicativos que exigem um provedor de banco de dados mais eficiente, robusto e escalonável, é recomendável que os clientes considerem usar o recurso Filestream disponível com Microsoft SQL Server. Para obter mais informações sobre SQL filestreams, consulte <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Aplicativos com transações que envolvem arquivos em um volume NTFS local e tabelas em um banco de dados SQL externo

Há classes de aplicativos que têm grandes necessidades de conjuntos de dados ou precisam ter atomicidade transacional em uma operação que envolva um banco de dados externo e um armazenamento local. Para esse cenário, é altamente recomendável que os desenvolvedores considerem usar SQL filestreams para executar operações de arquivo transacionais. Para obter mais informações sobre SQL filestreams, consulte <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Fechar & ação recomendada

O TxF é um conjunto complexo e com nuances de APIs que não são comumente usadas por aplicativos de terceiros. Com a possibilidade de que essas APIs possam não estar disponíveis em versões futuras do Windows e o fato de que há meios alternativos mais simples para alcançar muitos dos cenários para os quais o TxF foi desenvolvido, a Microsoft recomenda fortemente que os desenvolvedores investiguem esses meios alternativos em vez de criar uma dependência no TxF em seus aplicativos.

 

 
