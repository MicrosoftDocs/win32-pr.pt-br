---
description: Definir a propriedade SHORTFILENAMES faz com que nomes de arquivo curtos sejam usados para os nomes de arquivos de destino, em vez de nomes de arquivo longos. Ele não afeta os nomes de arquivo que o instalador procura na origem.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Propriedade SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb64d9f2078a1455aa79bfec077e6108f4a8a5bd9ced7d246c5fe588919b33d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628406"
---
# <a name="shortfilenames-property"></a>Propriedade SHORTFILENAMES

Definir a **propriedade SHORTFILENAMES** faz com que nomes de arquivo curtos sejam usados para os nomes de arquivos de destino, em vez de nomes de arquivo longos. Ele não afeta os nomes de arquivo que o instalador procura na origem.

## <a name="default-value"></a>Valor padrão

Nomes longos serão usados pelo instalador se a **propriedade SHORTFILENAMES** não estiver definida e o volume de destino for compatível com nomes longos. Nomes curtos são usados pelo instalador se o volume de destino não dá suporte a nomes longos.

## <a name="remarks"></a>Comentários

Quando a **propriedade SHORTFILENAMES** é definida, o instalador cria pastas e instala arquivos usando nomes de arquivos curtos de quaisquer pares curtos e \| longos listados na tabela Arquivo ou na [tabela Diretório](directory-table.md). [](file-table.md)

Os aplicativos podem usar a [**função GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) para recuperar a forma de caminho curto de um caminho de arquivo especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP. Consulte o [Windows instalador Run-Time para](windows-installer-portal.md) obter informações sobre o Windows service pack mínimo exigido por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

 
