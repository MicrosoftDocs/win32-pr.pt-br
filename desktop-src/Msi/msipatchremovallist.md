---
description: O instalador define o valor da propriedade MsiPatchRemovalList como uma lista de patches que estão sendo removidos durante a instalação.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propriedade MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93df2cdfc658875526c049ca7503e66a5c318df896a604a82c18751ac3358285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065976"
---
# <a name="msipatchremovallist-property"></a>Propriedade MsiPatchRemovalList

O instalador define o valor da propriedade **MsiPatchRemovalList** como uma lista de patches que estão sendo removidos durante a instalação. Os patches são representados na lista por seus GUIDs de código de patch separados por ponto e vírgula.

os desenvolvedores podem usar a propriedade **MsiPatchRemovalList** para criar um pacote Windows Installer ou patch que executa [ações personalizadas](custom-actions.md) sobre a remoção de um patch. A ação personalizada pode ser criada no pacote de instalação original, um patch que já foi aplicado ao pacote ou um patch que não é um [patch desinstalável](uninstallable-patches.md). A ação personalizada pode ser condicional na propriedade **MsiPatchRemovalList** nas tabelas de sequência. Consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md) para obter mais informações sobre a condicionalização de ações.

A ação personalizada pode obter os GUIDs dos patches que estão sendo removidos do valor da propriedade **MsiPatchRemovalList** . A ação personalizada pode determinar se o estado de instalação do patch é aplicado, obsoleto ou substituído chamando a função [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou a propriedade [**patchproperty**](patch-patchproperty.md) do [objeto patch](patch-object.md).

## <a name="remarks"></a>Comentários

Para obter mais informações sobre como remover patches, consulte [removendo patches](removing-patches.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador 3,0 ou posterior no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




