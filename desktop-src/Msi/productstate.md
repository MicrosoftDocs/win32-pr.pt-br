---
description: O instalador define a propriedade Productstate como o estado de instalação do produto na inicialização.
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: Propriedade productstate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759379"
---
# <a name="productstate-property"></a>Propriedade productstate

O instalador define a propriedade **productstate** como o estado de instalação do produto na inicialização. Essa propriedade é definida como um dos seguintes tipos de dados INSTALLstate retornados por [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).



| INSTALLSTATE             | Valor numérico | Estado de instalação do produto                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLstate \_ desconhecido    | -1            | O produto não é anunciado nem instalado. |
| INSTALLstate \_ anunciado | 1             | O produto é anunciado, mas não está instalado.    |
| INSTALLstate \_ ausente     | 2             | O produto está instalado para um usuário diferente.  |
| padrão INSTALLstate \_    | 5             | O produto está instalado para o usuário atual.  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 




