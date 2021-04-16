---
description: A propriedade EXECUTEmode especifica como o instalador executa as atualizações do sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propriedade EXECUTEmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758781"
---
# <a name="executemode-property"></a>Propriedade EXECUTEmode

A propriedade **executemode** especifica como o instalador executa as atualizações do sistema. Essa propriedade pode ser útil quando for necessário executar uma instalação sem realmente alterar o sistema. A propriedade pode ser definida como None para desabilitar as operações de atualização, como a instalação de arquivos e valores de registro.

Essa propriedade pode ter um dos dois valores a seguir. O instalador apenas examina a primeira letra do valor e não diferencia maiúsculas de minúsculas.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>None
</dt> <dd>

Nenhuma alteração é feita no sistema. O instalador executa a interface do usuário e, em seguida, consulta o banco de dados.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Prescritiva
</dt> <dd>

Todas as alterações no sistema são feitas por meio de execução de script. Esse é o modo padrão.

</dd> </dl>

## <a name="default-value"></a>Valor padrão

Se essa propriedade não for definida, o modo de execução usa como padrão o script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




