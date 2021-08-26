---
description: Assim como um aplicativo requer um DC (contexto de dispositivo de exibição) antes que possa começar a desenhar na área do cliente de uma janela, ele precisa de um DC de impressora para que possa começar a enviar a saída para uma impressora.
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: Contextos de dispositivo de impressora (documentos e impressão)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c868d5bf8247375375b33bcb034a70bd6f28c5b9104b61e264543a63281069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947396"
---
# <a name="printer-device-contexts-documents-and-printing"></a>Contextos de dispositivo de impressora (documentos e impressão)

Assim como um aplicativo requer um DC (contexto de dispositivo de exibição) antes que possa começar a desenhar na área do cliente de uma janela, ele precisa de um DC de impressora para que possa começar a enviar a saída para uma impressora. Um controlador de domínio de impressora é semelhante a um DC de vídeo, pois é uma estrutura de dados interna que define um conjunto de objetos gráficos e seus atributos associados e especifica os modos gráficos que afetam a saída. Os objetos gráficos incluem uma caneta para desenho de linha, um pincel para pintura e preenchimento e uma fonte para saída de texto.

Ao contrário de um controlador de domínio de vídeo, um controlador de domínio de impressora não pertence ao componente de gerenciamento de janelas e não pode ser obtido chamando a função [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) . Em vez disso, um aplicativo deve chamar a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) ou [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) .

Se seu aplicativo chama a função [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) , ele deve fornecer um nome de porta e driver. Para recuperar esses nomes, chame a função [**Getprinter**](getprinter.md) ou [**EnumPrinters**](enumprinters.md) .

Se seu aplicativo chama a função [**PRINTDLGEX**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) e especifica o \_ valor de RETURNDC de PD no membro **flags** da estrutura [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa) , o sistema retorna um identificador para um contexto de dispositivo para a impressora selecionada pelo usuário. Para obter mais informações, consulte [Imprimir folha de propriedades](../dlgbox/print-property-sheet.md) e "usando a folha de propriedades Imprimir" em [usando caixas de diálogo comuns](../dlgbox/using-common-dialog-boxes.md).

 

 
