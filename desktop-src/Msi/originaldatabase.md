---
description: O Windows Installer define a propriedade OriginalDatabase como o caminho do banco de dados de instalação usado para iniciar a instalação.
ms.assetid: 985c70a4-1575-4226-a8c2-a7a21f7a0dbd
title: Propriedade OriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 592bc86a9ef53602f686e48b3c98dad17a49cfe1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758768"
---
# <a name="originaldatabase-property"></a>Propriedade OriginalDatabase

O Windows Installer define a propriedade **OriginalDatabase** como o caminho do banco de dados de instalação usado para iniciar a instalação. Se a instalação for iniciada a partir de uma linha de comando, o valor dependerá se a opção de recache de pacote (o sinalizador-v) está presente na propriedade [**REinstallmode**](reinstallmode.md) .



| Método de instalação                                                                                                                                                                                  | Valor de OriginalDatabase                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Qualquer instalação iniciada invocando o caminho do pacote de instalação (arquivo. msi).                                                                                                              | Caminho para o pacote de instalação (arquivo. msi). |
| Instalação iniciada a partir de uma linha de comando. A instalação não é iniciada a partir de um caminho de pacote. A opção de recache (sinalizador-v) está presente na propriedade [**REinstallmode**](reinstallmode.md) .     | Caminho para o banco de dados na origem.           |
| Instalação iniciada a partir de uma linha de comando. A instalação não é iniciada a partir de um caminho de pacote. A opção de recache (sinalizador-v) não está presente na propriedade [**REinstallmode**](reinstallmode.md) . | Caminho para o banco de dados armazenado em cache.                  |



 

## <a name="remarks"></a>Comentários

Durante uma instalação pela primeira vez, uma ação personalizada sequenciada antes da [ação resolver](resolvesource-action.md) pode usar a propriedade **OriginalDatabase** para determinar o local da origem da instalação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




