---
description: Esta tabela contém os arquivos de ícone. Cada ícone da tabela é copiado para um arquivo como parte do anúncio do produto a ser usado para atalhos anunciados e servidores OLE. Consulte limitações de OLE em fluxos.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Tabela de ícones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169189"
---
# <a name="icon-table"></a>Tabela de ícones

Esta tabela contém os arquivos de ícone. Cada ícone da tabela é copiado para um arquivo como parte do anúncio do produto a ser usado para atalhos anunciados e servidores OLE. Consulte [limitações de OLE em fluxos](ole-limitations-on-streams.md).

A tabela de ícones tem as colunas a seguir.



| Coluna | Tipo                         | Chave | Nullable |
|--------|------------------------------|-----|----------|
| Nome   | [Identificador](identifier.md) | S   | N        |
| Dados   | [Binary](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes
</dt> <dd>

Nome do arquivo de ícone.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado
</dt> <dd>

Os dados do ícone binário no formato PE (. dll ou. exe) ou ícone (. ico).

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é referida quando a [ação PublishProduct](publishproduct-action.md) é executada.

Os ícones para atalhos, extensões de nome de arquivo e CLSIDs devem ser armazenados em arquivos separados do próprio arquivo de destino. Isso é necessário porque o instalador deve copiar apenas os arquivos de ícone pequeno para o computador do usuário ao anunciar o recurso. Portanto, um desenvolvedor de um pacote de instalação precisa criar arquivos separados contendo apenas os ícones. Esses arquivos de ícone são armazenados como dados binários na tabela de ícones.

Os arquivos de ícone que estão associados estritamente com extensões de nome de arquivo ou CLSIDs podem ter qualquer extensão, como. ico. No entanto, os arquivos de ícone associados a atalhos devem estar no formato binário EXE e devem ser nomeados de forma que sua extensão corresponda à extensão do destino. O atalho não funcionará se essa regra não for seguida. Por exemplo, se um atalho for apontar para um recurso com o arquivo de chave Red.bar, o arquivo de ícone também deverá ter a extensão. bar. Vários ícones podem ser inserida no mesmo arquivo de ícone, desde que todos os arquivos de destino tenham a mesma extensão.

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE29](ice29.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE50](ice50.md)  
</dl>

 

 



