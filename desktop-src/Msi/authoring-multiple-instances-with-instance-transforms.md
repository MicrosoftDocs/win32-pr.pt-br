---
description: Para instalar várias instâncias de um produto de um pacote Windows Installer, você precisa criar um pacote de instalação base para o produto e uma transformação de instância para cada instância a ser instalada, além da instância base.
ms.assetid: fef49dda-503f-4b13-8763-70cb2ee0df5d
title: Criando várias instâncias com transformações de instância
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61424efbf08ea3e726594a3073f4ce7483af57d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778734"
---
# <a name="authoring-multiple-instances-with-instance-transforms"></a>Criando várias instâncias com transformações de instância

Para instalar várias instâncias de um produto de um pacote Windows Installer, você precisa criar um pacote de instalação base para o produto e uma transformação de instância para cada instância a ser instalada, além da instância base. Use as seguintes diretrizes ao criar seu pacote base e transformações:

-   Seu aplicativo de instalação pode verificar a presença do instalador em execução em uma versão do Windows Vista, no Windows Server 2003, no Windows XP com Service Pack 1 (SP1) e no Windows Installer 3,0 redistribuível. Qualquer uma dessas versões de instalador (ou posteriores) é necessária para instalar várias instâncias de um único pacote usando um código de produto – alteração de transformação.
-   Cada instância deve ter um código de produto e um identificador de instância exclusivos. Você pode definir uma propriedade no pacote base, o valor que pode ser definido como o identificador de instância.
-   Para manter os arquivos de cada instância isoladas, o pacote base deve instalar arquivos em um local de diretório que dependa do identificador de instância.
-   Para manter os dados de não-arquivo de cada instância isolada, o pacote base deve coletar dados de não-arquivo em conjuntos de componentes para cada instância. Os componentes apropriados devem ser instalados com base em instruções condicionais que dependem do identificador da instância.
-   Crie uma transformação de instância para cada instância que está sendo instalada, além da instância base. O pacote base pode instalar sua própria instância.
-   A transformação da instância deve alterar o código do produto e o identificador para cada instância.
-   É recomendável que a transformação do produto também altere o nome do produto para que a instância seja prontamente diferenciada em Adicionar ou remover programas por meio do painel de controle.
-   Se a transformação de instância instalar arquivos, eles deverão ser instalados em um diretório que depende do identificador de instância.
-   Todos os dados que não são de arquivo, como chaves do registro, devem incluir o nome da instância em seu caminho para evitar colisões. Isso pode ser feito usando a propriedade cujo valor é o identificador de instância no caminho, conforme mostrado pelo exemplo a seguir de uma [tabela de registro](registry-table.md).



| Registro | Root | Chave                                            | Nome         | Valor           | Componente\_      |
|----------|------|------------------------------------------------|--------------|-----------------|------------------|
| Reg1     | 1    | Software \\ Microsoft \\ MyProduct \\ \[ InstanceId\] | InstanceGuid | \[ProductCode\] | NonFileDataComp1 |



 

Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md) e [Instalando várias instâncias com transformações de instância](installing-multiple-instances-with-instance-transforms.md).

 

 



