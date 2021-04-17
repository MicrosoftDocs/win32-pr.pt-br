---
description: O instalador define a propriedade TempFolder como o caminho completo para a pasta Temp. Os autores não devem precisar definir a propriedade TempFolder.
ms.assetid: 841dd1b3-249c-49e1-b462-82da65b4b023
title: Propriedade TempFolder
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbf042086d8bb174a02a7b421ced1133a70016e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752632"
---
# <a name="tempfolder-property"></a>Propriedade TempFolder

O instalador define a propriedade **TempFolder** como o caminho completo para a pasta Temp.

Os autores não devem precisar definir a propriedade **TempFolder** . Windows Installer usa a função [**GetTempPath**](/windows/win32/api/fileapi/nf-fileapi-gettemppatha) para recuperar o caminho do diretório designado para arquivos temporários e para definir essa propriedade.

## <a name="remarks"></a>Comentários

Um valor comum para essa propriedade é C: \\ Temp.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
