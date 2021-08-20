---
description: A propriedade SourceDir é o diretório raiz que contém o arquivo de gabinete de origem ou a árvore do arquivo de origem do pacote de instalação. Esse valor é usado para a resolução de diretório.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Propriedade SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 163fde883708f1c842a2cc1483f7558accb79129446554252dc3d18f2a2fe939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117989984"
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
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




