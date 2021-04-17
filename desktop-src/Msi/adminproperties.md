---
description: As Adminproperties devem ser criadas na tabela de propriedades.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propriedade adminproperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 739a0e29526ac7c6d9c094bc492cde1d04cdd0f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757132"
---
# <a name="adminproperties-property"></a>Propriedade adminproperties

As **adminproperties** devem ser criadas na tabela de [Propriedades](property-table.md). O valor de **adminproperties** é uma lista de nomes de propriedade separados por ponto e vírgula. O instalador salva os valores dessas propriedades listadas no momento de uma [instalação administrativa](administrative-installation.md). Quando os usuários instalam a partir da imagem administrativa, a instalação usa os valores salvos das propriedades, em vez dos valores no arquivo. msi.

## <a name="remarks"></a>Comentários

Os nomes de propriedade na lista podem ser letras maiúsculas e minúsculas (propriedades particulares) ou todas as letras maiúsculas (propriedades públicas).

Essa propriedade nunca deve terminar com um ponto e vírgula.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




