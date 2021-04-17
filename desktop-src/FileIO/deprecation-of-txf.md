---
description: Este tópico discute alternativas ao uso da API de NTFS Transacional (TxF) em cenários de uso comuns.
ms.assetid: 9ee26e7e-990e-4cd3-8180-f0fcaac2b752
title: Alternativas ao uso do NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc69974f27abfba0323ea4d3f16a720e5e99e69d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759419"
---
# <a name="alternatives-to-using-transactional-ntfs"></a>Alternativas ao uso do NTFS Transacional

-   [Resumo](#abstract)
-   [Introdução](#introduction)
-   [Alternativas para o TxF por cenário](#alternatives-to-txf-by-scenario)
-   [Aplicativos atualizando um único arquivo com dados "como documentos"](#applications-updating-a-single-file-with-document-like-data)
-   [Aplicativos que executam atualizações em vários arquivos e/ou no hive do registro](#applications-performing-updates-to-multiple-files-andor-to-the-registry-hive)
-   [Aplicativos que gerenciam um conjunto de dados estruturados](#applications-managing-a-set-of-structured-data)
-   [Aplicativos com transações envolvendo arquivos em um volume NTFS local e tabelas em um banco de dados SQL externo](#applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database)
-   [Fechando & ação recomendada](/windows)

## <a name="abstract"></a>Resumo

A Microsoft recomenda enfaticamente que os desenvolvedores investiguem a utilização das alternativas discutidas (ou em alguns casos, investigue outras alternativas) em vez de adotar uma plataforma de API que pode não estar disponível em versões futuras do Windows.

## <a name="introduction"></a>Introdução

O TxF foi introduzido com o Windows Vista como um meio de introduzir transações de arquivo atômica para o Windows. Ele permite que os desenvolvedores do Windows tenham atomicidade transacional para operações de arquivo em transações com um único arquivo, em transações que envolvem vários arquivos e em transações que abrangem várias fontes – como o registro (por meio de TxR) e bancos de dados (como SQL). Embora o TxF seja um conjunto poderoso de APIs, houve um interesse de desenvolvedor extremamente limitado nessa plataforma de API desde o Windows Vista, principalmente devido à sua complexidade e a várias nuances que os desenvolvedores precisam considerar como parte do desenvolvimento de aplicativos. Como resultado, a Microsoft está considerando a substituição de APIs de TxF em uma versão futura do Windows para concentrar os esforços de desenvolvimento e manutenção em outros recursos e APIs que têm mais valor para uma maior parte dos clientes. A próxima seção descreve os métodos alternativos de exemplo para obter resultados semelhantes à medida que o TxF faria para vários tipos de cenários de aplicativos.

## <a name="alternatives-to-txf-by-scenario"></a>Alternativas para o TxF por cenário

Com as limitações descritas acima, os desenvolvedores devem investigar alternativas ao TxF para abranger cenários de aplicativos que não são atendidos pelo TxF. Discutimos aqui algumas alternativas sugeridas para usos comuns do TxF para os desenvolvedores considerarem. Observe que essa lista não é exaustiva nem completa.

## <a name="applications-updating-a-single-file-with-document-like-data"></a>Aplicativos atualizando um único arquivo com dados "como documentos"

Muitos aplicativos que lidam com dados "como documentos" tendem a carregar o documento inteiro na memória, operar nele e, em seguida, escrevê-lo novamente para salvar as alterações. A atomicidade necessária aqui é que as alterações são completamente aplicadas ou não aplicadas, pois um estado inconsistente renderizaria o arquivo corrompido. Uma abordagem comum é gravar o documento em um novo arquivo e, em seguida, substituir o arquivo original pelo novo. Um método para fazer isso é com a API [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) .

## <a name="applications-performing-updates-to-multiple-files-andor-to-the-registry-hive"></a>Aplicativos que executam atualizações em vários arquivos e/ou no hive do registro

Há muitos aplicativos que precisam executar atomicamente uma atualização para um conjunto de arquivos e para o registro. Esse cenário é mais comumente obtido por meio de um aplicativo de instalador, como Windows Installer. Para obter mais informações sobre Windows Installer, consulte [Windows Installer](/windows/desktop/Msi/windows-installer-portal).

## <a name="applications-managing-a-set-of-structured-data"></a>Aplicativos que gerenciam um conjunto de dados estruturados

Muitos aplicativos gerenciam um conjunto de estruturas de dados proprietários de tipos variados como um meio de armazenar dados. Um desafio significativo para esses aplicativos é o processo de manutenção da integridade de ponteiros/referências internos se ocorrer uma falha durante uma operação de atualização. Criar o mecanismo para isso é, na verdade, um "problema difícil" e, portanto, a maioria dos aplicativos dependerá de um servidor de banco de dados verdadeiro para gerenciar seu conjunto de dados.

Duas sugestões para ajudar a gerenciar dados estruturados são:

-   A Microsoft fornece a caixa de entrada do ESE (mecanismo de armazenamento extensível) no Windows para permitir que os aplicativos executem operações de recuperação e atualização de dados transacionadas. Para obter mais informações sobre o ESE (mecanismo de armazenamento extensível), consulte <https://msdn.microsoft.com/library/gg269259.aspx> .
-   Para aplicativos que exigem um provedor de banco de dados mais potente, robusto e escalonável, é recomendável que os clientes considerem o uso do recurso FileStream disponível com Microsoft SQL Server. Para obter mais informações sobre o SQL filestreams, consulte <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="applications-with-transactions-involving-files-on-a-local-ntfs-volume-and-tables-in-an-external-sql-database"></a>Aplicativos com transações envolvendo arquivos em um volume NTFS local e tabelas em um banco de dados SQL externo

Há classes de aplicativos que têm grandes necessidades de conjuntos de dados, ou precisam ter atomicidade transacional em uma operação que envolva um armazenamento local e um banco de dados externo. Para esse cenário, é altamente recomendável que os desenvolvedores considerem o uso de filestreams do SQL para executar operações de arquivo transacionais. Para obter mais informações sobre o SQL filestreams, consulte <https://technet.microsoft.com/library/bb933993.aspx> .

## <a name="closing--recommended-action"></a>Fechando & ação recomendada

O TxF é um conjunto complexo e nuance de APIs que não são normalmente usadas por aplicativos de terceiros. Com a possibilidade de que essas APIs possam não estar disponíveis em versões futuras do Windows, e o fato de que há um meio mais simples de atingir muitos dos cenários para os quais o TxF foi desenvolvido, a Microsoft recomenda enfaticamente que os desenvolvedores investiguem esses meios alternativos em vez de criar uma dependência no TxF em seus aplicativos.

 

 
