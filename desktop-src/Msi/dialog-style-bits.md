---
description: O estilo de uma caixa de diálogo é especificado na coluna atributos da tabela de diálogo por uma palavra de 32 bits composta de sinalizadores de bits de estilo.
ms.assetid: aad719e8-86b3-4b2b-b417-db55013f8d3a
title: Bits de estilo de caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f22392ef9a88c547bd8fde5bc7df2f4839d66ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757124"
---
# <a name="dialog-style-bits"></a>Bits de estilo de caixa de diálogo

O estilo de uma caixa de diálogo é especificado na coluna atributos da [tabela de diálogo](dialog-table.md) por uma palavra de 32 bits composta de sinalizadores de bits de estilo.

A lista a seguir fornece links para descrições de bits de estilo de caixa de diálogo reservada.



| Nome                                                      | Decimal | Hexadecimal | Constante                                                                                                                                       |
|-----------------------------------------------------------|---------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Visível](visible-dialog-style-bit.md)                   | 1       | 0x00000001  | **msidbDialogAttributesVisible**                                                                                                               |
| [Modal](modal-dialog-style-bit.md)                       | 2       | 0x00000002  | **msidbDialogAttributesModal**                                                                                                                 |
| [Minimizar](minimize-dialog-style-bit.md)                 | 4       | 0x00000004  | **msidbDialogAttributesMinimize**                                                                                                              |
| [SysModal](sysmodal-dialog-style-bit.md)                 | 8       | 0x00000008  | **msidbDialogAttributesSysModal**                                                                                                              |
| [KeepModeless](keepmodeless-dialog-style-bit.md)         | 16      | 0x00000010  | **msidbDialogAttributesKeepModeless**                                                                                                          |
| [TrackDiskSpace](trackdiskspace-dialog-style-bit.md)     | 32      | 0x00000020  | **msidbDialogAttributesTrackDiskSpace**                                                                                                        |
| [UseCustomPalette](usecustompalette-dialog-style-bit.md) | 64      | 0x00000040  | **msidbDialogAttributesUseCustomPalette**                                                                                                      |
| [RTLRO](rtlro-dialog-style-bit.md)                       | 128     | 0x00000080  | **msidbDialogAttributesRTLRO**                                                                                                                 |
| [RightAligned](rightaligned-dialog-style-bit.md)         | 256     | 0x00000100  | **msidbDialogAttributesRightAligned**                                                                                                          |
| [LeftScroll](leftscroll-dialog-style-bit.md)             | 512     | 0x00000200  | **msidbDialogAttributesLeftScroll**                                                                                                            |
| [BiDi](bidi-dialog-style-bit.md)                         | 896     | 0x00000380  | **msidbDialogAttributesBiDi**  =  **msidbDialogAttributesRTLRO** \| **msidbDialogAttributesRightAligned** \| **msidbDialogAttributesLeftScroll** |
| [Erro](error-dialog-style-bit.md)                       | 65536   | 0x00010000  | **msidbDialogAttributesError**                                                                                                                 |



 

 

 



