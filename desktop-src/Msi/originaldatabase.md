---
description: O Windows instalador define a propriedade OriginalDatabase como o caminho do banco de dados de instalação usado para iniciar a instalação.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propriedade OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28b8ec6b77d013ee89d081c0ff20e3ad00750454e1fa9299d364fdb94e69ccb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145529"
---
# <a name="originaldatabase-property"></a>Propriedade OriginalDatabase

O Windows instalador define a **propriedade OriginalDatabase** como o caminho do banco de dados de instalação usado para iniciar a instalação. Se a instalação for lançada de uma linha de comando, o valor dependerá se a opção de pacote recache (o sinalizador -v) está presente na [**propriedade REINSTALLMODE.**](reinstallmode.md)



| Método de instalação                                                                                                                                                                                  | Valor originalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Qualquer instalação iniciada invocando o caminho do pacote de instalação (.msi arquivo).                                                                                                              | Caminho para o pacote de instalação (.msi arquivo). |
| Instalação lançada de uma linha de comando. A instalação não é lançada de um caminho de pacote. A opção recache (-v flag) está presente na [**propriedade REINSTALLMODE.**](reinstallmode.md)     | Caminho para o banco de dados na origem.           |
| Instalação lançada de uma linha de comando. A instalação não é lançada de um caminho de pacote. A opção recache (-v flag) não está presente na [**propriedade REINSTALLMODE.**](reinstallmode.md) | Caminho para o banco de dados armazenado em cache.                  |



 

## <a name="remarks"></a>Comentários

Durante uma primeira instalação, uma ação personalizada sequenciada antes da [ação ResolveSource](resolvesource-action.md) pode usar a propriedade **OriginalDatabase** para determinar o local da origem da instalação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




