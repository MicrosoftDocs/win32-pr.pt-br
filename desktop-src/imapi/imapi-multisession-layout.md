---
title: Layout de várias sessões do IMAPi
description: O IMAPi fornece aos desenvolvedores de aplicativos a capacidade de criar imagens do sistema de arquivos ISO 9660 e UDF e gravá-las em CD, DVD e Blu-Ray \ 8482; mídia óptica.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d816d293a3474f46dc3a48577a46615672103099dc2aa561d393953f29ccf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249399"
---
# <a name="imapi-multisession-layout"></a>Layout de várias sessões do IMAPi

O IMAPi fornece aos desenvolvedores de aplicativos a capacidade de criar imagens do sistema de arquivos ISO 9660 e UDF e gravá-las em CD, DVD e Blu-Ray™ mídia óptica. com o Windows 7, o imapi fornece suporte adicional para a gravação de várias sessões em DVD e Blu-Ray™ mídia regravável.

A documentação a seguir detalha o layout do disco que o IMAPi utiliza para implementar várias sessões. Essas informações devem ser usadas para garantir a interoperabilidade entre o IMAPi e outros softwares de gravação, além de permitir que os desenvolvedores desse software criem imagens de disco de várias sessões compatíveis com o IMAPi.

> [!Note]  
> Para obter um exemplo detalhando a criação de um disco de várias sessões, consulte [criando um disco de várias sessões](creating-a-multisession-disc.md).

 

## <a name="multisession-on-sequential-media"></a>Várias sessões em mídia sequencial

A implementação de IMAPi de várias sessões em mídia sequencial tem suporte para uso com mídia de CD-R, CD-RW, DVD-R, DVD + R e Blu-Ray™. O IMAPi usa o modo de gravação de sessão em uma vez para o CD-RW e, como resultado, nesse cenário, o formato é considerado um tipo de mídia sequencial.

Em um cenário que envolve a multisessão em mídia sequencial usando UDF, o IMAPi grava as estruturas de âncora (o descritor de volume de âncora UDF-AVDP), estruturas de volume (sequência de descritor de volume UDF-VDS) e as estruturas de metadados do sistema de arquivos (descritor de conjunto de arquivos UDF-FSD) no início de cada nova sessão, conforme descrita no

![Diagrama que mostra a estrutura de metadados do sistema de arquivos com o "ponto de montagem da importação/F S" indicado com uma seta vermelha na "âncora" da sessão física 2.](images/multises1.png)

> [!Note]  
> Esta figura ilustra o layout do disco IMAPi ao usar o UDF 2,50 com metadados redundantes.

 

Os dados armazenados em mídias gravadas em sequência consistem em um número de sessões físicas. Cada sessão contém um sistema de arquivos completo que representa os dados do usuário como um conjunto de arquivos organizados em diretórios. Os metadados do sistema de arquivos consistem em várias estruturas de dados organizadas hierarquicamente. Na parte superior da hierarquia residem as estruturas de âncora (AVDP) em endereços de bloco lógico predefinidos (LBAs). As estruturas de âncora especificam os locais das estruturas de próximo nível que não têm endereços predefinidos. O próximo nível de hierarquia após as estruturas de ancoragem contém as estruturas de volume (VDS) que descrevem as propriedades do volume e referenciando as FSD (estruturas de metadados do sistema de arquivos) que, por sua vez, descrevem arquivos e diretórios individuais.

## <a name="multisession-on-rewritable-media"></a>Várias sessões em mídia regravável

A abordagem para mídia sequencial descrita na seção anterior é incompatível com mídia regravável (não sequencial). Esses formatos de mídia incluem DVD-RW, DVD + RW, DVD-RAM, Blu-Ray™ regravável e outras mídias graváveis aleatórias, como discos Iomega REV. A mídia regravável não dá suporte ao conceito de sessões físicas correspondentes às sessões lógicas, que são incrementos individuais confirmados por um aplicativo de mestre. Apenas uma única sessão física é exposta, que é uma área que começa no início do disco que representa a área endereçável inteira que tem o potencial de conter várias sessões lógicas.

> [!Note]  
> Embora o DVD-RW seja uma exceção em que ele dá suporte ao conceito de uma sessão física no modo sequencial, atualmente esse recurso não é suportado pelo IMAPi.

 

Para resolver a falta de um mapeamento de um para um entre sessões físicas e lógicas em formatos regraváveis, o IMAPi atualiza seletivamente as estruturas de âncora (AVDP) na *primeira* sessão lógica para apontar para as novas estruturas de volume (VDS) e as estruturas de metadados do sistema de arquivos (FSD) no início da *última* sessão lógica, conforme descrito no diagrama a seguir:

![Diagrama que mostra a estrutura de metadados do sistema de arquivos com o "ponto de montagem da importação/F S" indicado com uma seta vermelha na "âncora" da sessão lógica 1.](images/multises2.png)

> [!Note]  
> Esta figura ilustra o layout do disco IMAPi ao usar o UDF 2,50 com metadados redundantes.

 

Ao adicionar uma nova sessão lógica a um disco regravável, o IMAPi primeiro determina o fim da última sessão lógica analisando os metadados do volume (VDS). Em seguida, o IMAPi adiciona a nova sessão lógica, completa com nova âncora (AVDP), volume (VDS) e estruturas de metadados do sistema de arquivos (FSD), fisicamente contígua com a sessão lógica gravada anteriormente. A etapa final exige que as estruturas de âncora (AVDP) no início da primeira sessão lógica sejam atualizadas para apontar para as estruturas de volume (VDS) na *nova* sessão lógica. O resultado operacional é o mesmo que com mídia sequencial.

## <a name="additional-recommendations"></a>Recomendações adicionais

-   **Layout de partição**

    Para obter o IMAPi compatibilidade, é recomendável que os desenvolvedores de software de gravação de terceiros usem os layouts de disco descritos nesta documentação. Os desenvolvedores devem evitar layouts com partições de sistema de arquivos ocupando todo o disco, pois isso requer a gravação de aplicativos para localizar espaço livre nas partições existentes sempre que os dados precisam ser anexados ao disco. Muitas vezes, os aplicativos de gravação realizam isso utilizando marcadores proprietários no disco para indicar quanto espaço está realmente ocupado pelos dados do usuário. Esses layouts de disco são incompatíveis com o IMAPi, pois os marcadores proprietários não são reconhecidos fora do aplicativo para o qual foram criados.

-   **Tipo de partição UDF**

    O IMAPi usa o tipo de partição UDF **somente leitura** em sua implementação de várias sessões na mídia regravável. os desenvolvedores de software de gravação de terceiros devem usar o tipo de partição UDF **somente leitura** para obter compatibilidade com Windows a gravação com o controle de mestre via imapi. Se outro tipo de partição UDF, como **regravável** , for usado, o IMAPI não poderá fornecer suporte à masterização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um disco de várias sessões](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




