---
description: Definir a propriedade TRANSFORMSSECURE como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propriedade TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770174"
---
# <a name="transformssecure-property"></a>Propriedade TRANSFORMSSECURE

Definir a propriedade **TRANSFORMSSECURE** como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação. Definir essa propriedade é como definir a [política TransformsSecure](transformssecure-policy.md) , exceto que o escopo é diferente. A configuração da política TransformsSecure se aplica a todos os pacotes instalados por um determinado usuário. A definição da propriedade **TRANSFORMSSECURE** se aplica ao pacote, independentemente do usuário.

A finalidade dessa propriedade é fornecer armazenamento de transformação seguro com usuários viajando do Windows 2000. Quando essa propriedade é definida, uma [instalação de manutenção](maintenance-installation.md) só pode usar a transformação do caminho especificado. Se o caminho não estiver disponível, a instalação de manutenção falhará. Portanto, uma origem para cada transformação segura deve residir no local da origem do pacote de instalação. Em seguida, se o instalador descobrir que a transformação está ausente no computador local, ele poderá restaurar a transformação dessa fonte.

## <a name="remarks"></a>Comentários

Windows Installer interpreta a propriedade [**TRANSFORMSATSOURCE**](transformsatsource.md) como a mesma que a propriedade **TRANSFORMSSECURE** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Transformações de banco de dados](database-transforms.md)
</dt> </dl>

 

 




