---
description: O instalador define a propriedade VersionNT64 como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriedade VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f6c0f2037891527f17feba92d7e9c8494aa622
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262068"
---
# <a name="versionnt64-property"></a>Propriedade VersionNT64

O instalador define a **propriedade VersionNT64** como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits. A propriedade será indefinida se o sistema operacional não for de 64 bits.

O valor é um inteiro: MajorVersion \* 100 + MinorVersion.

Por motivos de compatibilidade, a propriedade também [](template-summary.md) será indefinida se a propriedade Resumo do Modelo indicar que o pacote é para sistemas Intel (x86) de 32 bits e o sistema operacional não pode executar código Intel (x64) de 64 bits, como Windows 10 no ARM (ARM64).

> [!NOTE]
> A partir Windows 10 Build 21277, os builds arm64 no canal de dev do programa Windows Insider Preview têm suporte para aplicativos x64. Nesses builds arm64, a propriedade VersionNT64 é definida para pacotes x86.

## <a name="remarks"></a>Comentários

As expressões condicionais testam o Windows de 64 bits simplesmente usando o nome da propriedade ou verificando a versão usando um operador de comparação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4.0 ou Windows Installer 4.5 no Windows Server 2008 ou Windows Vista. Windows Installer windows server 2003 ou Windows XP Consulte os requisitos de [Windows Installer Run-Time](windows-installer-portal.md) para obter informações sobre o windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




