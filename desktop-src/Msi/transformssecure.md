---
description: Definir a propriedade TRANSFORMSSECURE como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação.
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: Propriedade TRANSFORMSSECURE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af3432b8f895d4d9f5d0fe643ef8106e01e28ad64fb2db177e968fbc13d88de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141629"
---
# <a name="transformssecure-property"></a>Propriedade TRANSFORMSSECURE

Definir a propriedade **TRANSFORMSSECURE** como 1 informa ao instalador que as transformações devem ser armazenadas em cache localmente no computador do usuário em um local em que o usuário não tem acesso de gravação. Definir essa propriedade é como definir a [política TransformsSecure](transformssecure-policy.md) , exceto que o escopo é diferente. A configuração da política TransformsSecure se aplica a todos os pacotes instalados por um determinado usuário. A definição da propriedade **TRANSFORMSSECURE** se aplica ao pacote, independentemente do usuário.

a finalidade dessa propriedade é fornecer armazenamento de transformação seguro com usuários de viagem de Windows 2000. Quando essa propriedade é definida, uma [instalação de manutenção](maintenance-installation.md) só pode usar a transformação do caminho especificado. Se o caminho não estiver disponível, a instalação de manutenção falhará. Portanto, uma origem para cada transformação segura deve residir no local da origem do pacote de instalação. Em seguida, se o instalador descobrir que a transformação está ausente no computador local, ele poderá restaurar a transformação dessa fonte.

## <a name="remarks"></a>Comentários

Windows O instalador interpreta a propriedade [**TRANSFORMSATSOURCE**](transformsatsource.md) para ser igual à propriedade **TRANSFORMSSECURE** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Transformações de banco de dados](database-transforms.md)
</dt> </dl>

 

 




