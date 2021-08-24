---
description: A presença da propriedade MSIINSTANCEGUID indica que um código de produto&\# 8211; a alteração da transformação está registrada para o produto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propriedade MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f67f3f307eebecc25857411c25471ac3b39a97d48b48d6cc2894636c47f673b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679526"
---
# <a name="msiinstanceguid-property"></a>Propriedade MSIINSTANCEGUID

A presença da propriedade **MSIINSTANCEGUID** indica que um código de produto – alteração de transformação está registrado para o produto. O valor da propriedade **MSIINSTANCEGUID** especifica qual instância de um produto deve ser usada para instalação. A propriedade **MSIINSTANCEGUID** só pode fazer referência a um produto que já tenha sido instalado com uma transformação de instância.

as transformações de instância são o código do produto – alterando transformações disponíveis com o instalador em execução no Windows Server 2003 ou Windows XP. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




