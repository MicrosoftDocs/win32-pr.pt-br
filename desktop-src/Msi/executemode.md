---
description: A propriedade EXECUTEMODE especifica como o instalador executa atualizações do sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propriedade EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 750b6c3a20ab05388fcd6926463dde8259440bd6087306b1bf0cc1a6c387cd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082866"
---
# <a name="executemode-property"></a>Propriedade EXECUTEMODE

A **propriedade EXECUTEMODE** especifica como o instalador executa atualizações do sistema. Essa propriedade pode ser útil quando é necessário executar uma instalação sem realmente alterar o sistema. A propriedade pode ser definida como Nenhum para desabilitar operações de atualização, como a instalação de arquivos e valores do Registro.

Essa propriedade pode ter um dos dois valores a seguir. O instalador examina apenas a primeira letra do valor e não reconhece maiúsculas de minúsculas.

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>Nenhum
</dt> <dd>

Nenhuma alteração é feita no sistema. O instalador executa a interface do usuário e consulta o banco de dados.

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script
</dt> <dd>

Todas as alterações no sistema são feitas por meio da execução do script. Esse é o modo padrão.

</dd> </dl>

## <a name="default-value"></a>Valor padrão

Se essa propriedade não estiver definida, o modo de execução assume Script como padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




