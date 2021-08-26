---
description: A propriedade MSINEWINSTANCE indica a instalação de uma nova instância de um produto com transformações de instância.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propriedade MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b26831f1171813d9df9e2c4124a4d6c24ea7efbf707fc5c15eefc9d6a8b1046
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082846"
---
# <a name="msinewinstance-property"></a>Propriedade MSINEWINSTANCE

A propriedade **MSINEWINSTANCE** indica a instalação de uma nova instância de um produto com transformações de instância. Essa propriedade dá suporte a várias instâncias por meio do código do produto – alterando transformações. O valor dessa propriedade é 1. A presença dessa propriedade na linha de comando requer que a propriedade [**TRANSformações**](transforms.md) também esteja presente. A primeira transformação listada em **TRANSformações** deve ser uma transformação de instância. Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md)

essa propriedade está disponível com o instalador que executa um sistema no Windows Server 2003 ou Windows XP.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows instalador 5,0 em Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou Windows Vista. Windows instalador no Windows Server 2003 ou Windows XP. consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre o service pack mínimo Windows exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




