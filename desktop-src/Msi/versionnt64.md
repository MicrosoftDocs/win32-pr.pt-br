---
description: O instalador definirá a propriedade VersionNT64 como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits.
ms.assetid: 190f8251-a377-4490-9de9-98d149185865
title: Propriedade VersionNT64
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a3b1b5a26b2ba45b859b6330bf153300e239074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757777"
---
# <a name="versionnt64-property"></a>Propriedade VersionNT64

O instalador definirá a propriedade **VersionNT64** como o número de versão do sistema operacional somente se o sistema estiver em execução em um computador de 64 bits. A propriedade será indefinida se o sistema operacional não for de 64 bits.

O valor é um inteiro: MajorVersion \* 100 + MinorVersion.

Por motivos de compatibilidade, a propriedade também será indefinida se a propriedade de [**Resumo do modelo**](template-summary.md) indicar que o pacote é para sistemas Intel de 32 bits e o sistema operacional é uma arquitetura de 64 bits que não é Intel64 ou x64 (como ARM64).

## <a name="remarks"></a>Comentários

As expressões condicionais testam as janelas de 64 bits simplesmente usando o nome da propriedade ou verificando a versão usando um operador de comparação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP, consulte os [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




