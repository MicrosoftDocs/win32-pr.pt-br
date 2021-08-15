---
description: A presença da propriedade MSIINSTANCEGUID indica que um código do produto&8211; a transformação de alteração é registrada \# no produto.
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

A presença da **propriedade MSIINSTANCEGUID** indica que uma transformação de alteração de código do produto está registrada no produto. O valor da **propriedade MSIINSTANCEGUID** especifica qual instância de um produto deve ser usada para instalação. A **propriedade MSIINSTANCEGUID** só pode referenciar um produto que já foi instalado com uma transformação de instância.

As transformares de instância são as transformação de código do produto que mudam disponíveis com o instalador em execução no Windows Server 2003 ou Windows XP. Para obter mais informações, [consulte Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows 2.0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




