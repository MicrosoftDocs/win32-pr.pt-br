---
description: A propriedade MSIPATCHREMOVE especifica a lista de patches a serem removidos durante uma instalação.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Propriedade MSIPATCHREMOVE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780950"
---
# <a name="msipatchremove-property"></a>Propriedade MSIPATCHREMOVE

A propriedade **MSIPATCHREMOVE** especifica a lista de patches a serem removidos durante uma instalação. Os patches individuais na lista são separados por ponto e vírgula e podem ser representados pelo GUID de código de patch ou pelo caminho completo para o patch. A função [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) e o método [**RemovePatches**](installer-removepatches.md) do objeto [instalador](installer-object.md) definem a propriedade **MSIPATCHREMOVE** .

A propriedade **MSIPATCHREMOVE** pode ser definida na linha de comando da seguinte maneira para remover um patch.

**msiexec/i A: \\Example.msi MSIPATCHREMOVE = c: \\ patches \\ qfe1. msp; { 0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




