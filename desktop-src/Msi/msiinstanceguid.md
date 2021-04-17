---
description: A presença da propriedade MSIINSTANCEGUID indica que um código de produto&\# 8211; a alteração da transformação está registrada para o produto.
ms.assetid: c39be15d-e10a-4055-bd81-aa7510a19fe4
title: Propriedade MSIINSTANCEGUID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c798d56cf3ede6a75a133dd7e0ec7f42c32e84f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768727"
---
# <a name="msiinstanceguid-property"></a>Propriedade MSIINSTANCEGUID

A presença da propriedade **MSIINSTANCEGUID** indica que um código de produto – alteração de transformação está registrado para o produto. O valor da propriedade **MSIINSTANCEGUID** especifica qual instância de um produto deve ser usada para instalação. A propriedade **MSIINSTANCEGUID** só pode fazer referência a um produto que já tenha sido instalado com uma transformação de instância.

As transformações de instância são código do produto – alterando transformações disponíveis com o instalador em execução no Windows Server 2003 ou no Windows XP. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




