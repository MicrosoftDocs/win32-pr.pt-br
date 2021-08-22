---
description: O instalador define a propriedade VersionNT64 como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriedade VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 285f97a6325df65ace9ff6620489697e6eeeb573761437bd0a826dec4dc31e5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526926"
---
# <a name="versionnt64-property"></a>Propriedade VersionNT64

O instalador define a **propriedade VersionNT64** como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits. A propriedade será indefinida se o sistema operacional não for de 64 bits.

O valor é um inteiro: MajorVersion \* 100 + MinorVersion.

Por motivos de compatibilidade, a propriedade também [](template-summary.md) será indefinida se a propriedade Resumo do Modelo indicar que o pacote é para sistemas Intel (x86) de 32 bits e o sistema operacional não pode executar código Intel (x64) de 64 bits, como Windows 10 no ARM (ARM64).

> [!NOTE]
> A partir Windows 10 Build 21277, os builds arm64 no canal de dev do programa Windows Insider Preview têm suporte para aplicativos x64. Nesses builds arm64, a propriedade VersionNT64 é definida para pacotes x86.

## <a name="remarks"></a>Comentários

As expressões condicionais testam para Windows de 64 bits simplesmente usando o nome da propriedade ou verificando a versão usando um operador de comparação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou no Windows XP Consulte os Requisitos do Run-Time [Installer Windows](windows-installer-portal.md) para obter informações sobre o Windows service pack mínimo exigido por uma versão do Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




