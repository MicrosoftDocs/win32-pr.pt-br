---
description: A propriedade MSINEWINSTANCE indica a instalação de uma nova instância de um produto com transformações de instância.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propriedade MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753261"
---
# <a name="msinewinstance-property"></a>Propriedade MSINEWINSTANCE

A propriedade **MSINEWINSTANCE** indica a instalação de uma nova instância de um produto com transformações de instância. Essa propriedade dá suporte a várias instâncias por meio do código do produto – alterando transformações. O valor dessa propriedade é 1. A presença dessa propriedade na linha de comando requer que a propriedade [**TRANSformações**](transforms.md) também esteja presente. A primeira transformação listada em **TRANSformações** deve ser uma transformação de instância. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md)

Essa propriedade está disponível com o instalador que executa um sistema no Windows Server 2003 ou no Windows XP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




