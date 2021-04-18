---
description: A propriedade SOURCElist é uma lista delimitada por ponto-e-vírgula de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: Propriedade SOURCElist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748568"
---
# <a name="sourcelist-property"></a>Propriedade SOURCElist

A propriedade **SourceList** é uma lista delimitada por ponto-e-vírgula de caminhos de origem de rede ou URL para o pacote de instalação do aplicativo. Essa lista é anexada ao final da lista de origem existente de cada usuário para o aplicativo. O instalador localiza uma fonte enumerando a lista de caminhos de origem e usa o primeiro local acessível encontrado. Somente essa fonte pode ser usada para o restante da instalação. Cada caminho especificado na lista de origem deve, portanto, ser um local que tenha uma origem completa para o aplicativo. A árvore de diretórios inteira em cada local de origem deve ser a mesma e deve incluir todos os arquivos de origem necessários, incluindo todos os gabinetes. Cada local deve ter um arquivo. msi com o mesmo nome de arquivo e código de produto.

## <a name="default-value"></a>Valor padrão

O instalador só verificará a propriedade **SourceList** se o produto ainda não tiver sido anunciado ou instalado. Em todos os outros casos, o instalador usa a lista de origem existente que está no registro.

## <a name="remarks"></a>Comentários

As fontes adicionadas usando a propriedade **SourceList** são adicionadas diretamente ao final da lista para cada tipo de origem e sempre vêm após a origem padrão especificada pela propriedade [**SourceDir**](sourcedir.md) .

Por Windows Installer o número de fontes na propriedade **SourceList** é ilimitado. [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) pode ser usado para adicionar fontes de rede.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Resiliência de origem](source-resiliency.md)
</dt> </dl>

 

 




