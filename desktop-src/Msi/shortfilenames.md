---
description: Definir a propriedade SHORTFILENAMES faz com que nomes de arquivo curtos sejam usados para os nomes dos arquivos de destino, em vez de nomes de arquivo longos. Ele não afeta os nomes de arquivo que o instalador procura na origem.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Propriedade SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752837"
---
# <a name="shortfilenames-property"></a>Propriedade SHORTFILENAMES

Definir a propriedade **SHORTFILENAMES** faz com que nomes de arquivo curtos sejam usados para os nomes dos arquivos de destino, em vez de nomes de arquivo longos. Ele não afeta os nomes de arquivo que o instalador procura na origem.

## <a name="default-value"></a>Valor padrão

Nomes longos são usados pelo instalador se a propriedade **SHORTFILENAMES** não estiver definida e o volume de destino der suporte a nomes longos. Nomes curtos são usados pelo instalador se o volume de destino não oferecer suporte a nomes longos.

## <a name="remarks"></a>Comentários

Quando a propriedade **SHORTFILENAMES** é definida, o instalador cria pastas e instala arquivos usando nomes de arquivo curtos a partir de qualquer par pequeno de \| pares listados na tabela de [arquivos](file-table.md) ou no [diretório](directory-table.md).

Os aplicativos podem usar a função [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) para recuperar a forma de caminho curto de um caminho de arquivo especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
