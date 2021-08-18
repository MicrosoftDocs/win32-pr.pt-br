---
description: O instalador define a propriedade TempFolder como o caminho completo para a pasta Temp. Os autores não devem precisar definir a propriedade TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propriedade TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5ded141982c12204eb5267357cedded6521eccb7cc47a3bf000b026faf9aed4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626497"
---
# <a name="tempfolder-property"></a>Propriedade TempFolder

O instalador define a propriedade **TempFolder** como o caminho completo para a pasta Temp.

Os autores não devem precisar definir a propriedade **TempFolder** . Windows O instalador usa a função [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) para recuperar o caminho do diretório designado para arquivos temporários e para definir essa propriedade.

## <a name="remarks"></a>Comentários

Um valor comum para essa propriedade é C: \\ Temp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
