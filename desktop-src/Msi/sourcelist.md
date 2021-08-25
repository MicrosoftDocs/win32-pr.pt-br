---
description: A propriedade SOURCELIST é uma lista delimitada por ponto e vírgula de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propriedade SOURCELIST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd0ab879d55481f71c663e4375a305232be576d0c923f67fa419530012d1ce89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893746"
---
# <a name="sourcelist-property"></a>Propriedade SOURCELIST

A **propriedade SOURCELIST** é uma lista delimitada por ponto e vírgula de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo. Essa lista é anexada ao final da lista de origem existente de cada usuário para o aplicativo. O instalador localiza uma origem enumerando a lista de caminhos de origem e usa o primeiro local acessível encontrado. Somente essa origem pode ser usada para o restante da instalação. Cada caminho especificado na lista de origem deve, portanto, estar em um local que tenha uma origem completa para o aplicativo. Toda a árvore de diretórios em cada local de origem deve ser a mesma e deve incluir todos os arquivos de origem necessários, incluindo os gabinetes. Cada local deve ter um arquivo .msi com o mesmo nome de arquivo e código do produto.

## <a name="default-value"></a>Valor padrão

O instalador verifica apenas a **propriedade SOURCELIST** se o produto ainda não foi anunciado ou instalado. Em todos os outros casos, o instalador usa a lista de origem existente que está no Registro.

## <a name="remarks"></a>Comentários

As fontes adicionadas usando a propriedade **SOURCELIST** são adicionadas diretamente ao final da lista para cada tipo de origem e sempre vêm após a origem padrão especificada pela [**propriedade SourceDir.**](sourcedir.md)

Por Windows Instalador, o número de fontes na **propriedade SOURCELIST** é ilimitado. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) pode ser usado para adicionar fontes de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




