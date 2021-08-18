---
description: Para instalar várias instâncias de um produto de um pacote do instalador do Windows, você precisa autor de um pacote de instalação base para o produto e uma transformação de instância para cada instância a ser instalada além da instância base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Como autor de várias instâncias com transformações de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efac957d5e0e82665cb1ba20aeb42fe9b60293699c5c3fd97f5e6a6f1abf58a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745906"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Como autor de várias instâncias com transformações de instância

Para instalar várias instâncias de um produto de um pacote do instalador do Windows, você precisa autor de um pacote de instalação base para o produto e uma transformação de instância para cada instância a ser instalada além da instância base. Use as seguintes diretrizes ao autorizar seu pacote base e transformar:

-   Seu aplicativo de instalação pode verificar a presença do instalador em execução em uma versão do Windows Vista, Windows Server 2003, Windows XP com Service Pack 1 (SP1) e o Windows Installer 3.0 redistribuível. Qualquer uma dessas versões do instalador (ou posterior) é necessária para instalar várias instâncias de um único pacote usando uma transformação de alteração de código do produto.
-   Cada instância deve ter um código de produto exclusivo e um identificador de instância. Você pode definir uma propriedade no pacote base, o valor do qual pode ser definido como o identificador de instância.
-   Para manter os arquivos de cada instância isolada, o pacote base deve instalar arquivos em um local de diretório que dependa do identificador da instância.
-   Para manter os dados não arquivos de cada instância isolada, o pacote base deve coletar dados não arquivos em conjuntos de componentes para cada instância. Os componentes apropriados devem ser instalados com base em instruções condicionais que dependem do identificador de instância.
-   Autor de uma transformação de instância para cada instância que está sendo instalada, além da instância base. O pacote base pode instalar sua própria instância.
-   A transformação da instância deve alterar o código do produto e o identificador de cada instância.
-   É recomendável que a transformação do produto também altere o nome do produto para que a instância seja prontamente diferenciada em Adicionar/Remover Programas por meio de Painel de Controle.
-   Se a transformação de instância instalar arquivos, eles deverão ser instalados em um diretório que dependa do identificador de instância.
-   Todos os dados não arquivos, como chaves do Registro, devem incluir o nome da instância em seu caminho para evitar colisões. Isso pode ser feito usando a propriedade cujo valor é o identificador de instância no caminho, conforme mostrado pelo exemplo a seguir de [uma Tabela do Registro](registry-table.md).



| Registro | Root | Chave                                            | Nome         | Valor           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | InstanceId \\ do Software Microsoft \\ MyProduct \\ \[\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Para obter mais informações, [consulte Instalando várias instâncias](installing-multiple-instances-of-products-and-patches.md) de produtos e patches e Instalando várias [instâncias com transformações de instância](installing-multiple-instances-with-instance-transforms.md).

 

 



