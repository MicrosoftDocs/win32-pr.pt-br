---
description: A propriedade SourceDir é o diretório raiz que contém o arquivo de gabinete de origem ou a árvore do arquivo de origem do pacote de instalação. Esse valor é usado para a resolução de diretório.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Propriedade SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759374"
---
# <a name="sourcedir-property"></a>Propriedade SourceDir

A propriedade **SourceDir** é o diretório raiz que contém o arquivo de gabinete de origem ou a árvore do arquivo de origem do pacote de instalação. Esse valor é usado para a resolução de diretório.

## <a name="default-value"></a>Valor padrão

O diretório que contém o pacote de instalação.

## <a name="remarks"></a>Comentários

A [ação de resolução](resolvesource-action.md) deve ser chamada antes de usar a **Propriedade SourceDir** em qualquer expressão ou tentar recuperar o valor de **SourceDir** com [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya). A ação de resolução não deve ser executada enquanto a origem não estiver disponível, como ao desinstalar um aplicativo, pois isso pode causar um aviso indesejado para a mídia de origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




