---
description: As Adminproperties devem ser criadas na tabela de propriedades.
ms.assetid: 91dd58cf-6c8c-4d20-a829-c43301a30d7f
title: Propriedade adminproperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f59d2452e244bd22110ab918dff61279bf9d27f3c8735f37474aea894d0d02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078126"
---
# <a name="adminproperties-property"></a>Propriedade adminproperties

As **adminproperties** devem ser criadas na tabela de [Propriedades](property-table.md). O valor de **adminproperties** é uma lista de nomes de propriedade separados por ponto e vírgula. O instalador salva os valores dessas propriedades listadas no momento de uma [instalação administrativa](administrative-installation.md). Quando os usuários instalam a partir da imagem administrativa, a instalação usa os valores salvos das propriedades, em vez dos valores no arquivo de .msi.

## <a name="remarks"></a>Comentários

Os nomes de propriedade na lista podem ser letras maiúsculas e minúsculas (propriedades particulares) ou todas as letras maiúsculas (propriedades públicas).

Essa propriedade nunca deve terminar com um ponto e vírgula.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




