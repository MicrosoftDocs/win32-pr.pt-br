---
description: Definir essa propriedade é como definir a política de política TransformsAtSource, exceto que o escopo é diferente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Propriedade TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785423"
---
# <a name="transformsatsource-property"></a>Propriedade TRANSFORMSATSOURCE

Definir essa propriedade é como definir a política de [política TransformsAtSource](transformsatsource-policy.md) , exceto que o escopo é diferente. A configuração da política TransformsAtSource se aplica a todos os pacotes instalados por um determinado usuário. A definição da propriedade **TRANSFORMSATSOURCE** se aplica ao pacote, independentemente dos usuários.

## <a name="remarks"></a>Comentários

Windows Installer interpreta a propriedade **TRANSFORMSATSOURCE** como se fosse a propriedade [**TRANSFORMSSECURE**](transformssecure.md) . Se o sinalizador @ for passado na propriedade [**TRANSformações**](transforms.md) , Windows Installer tratará as transformações na lista como [transformações de origem segura](secure-at-source-transforms.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




