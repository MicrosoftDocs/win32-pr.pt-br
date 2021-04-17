---
description: A propriedade date é o mês, o dia e o ano atuais como uma cadeia de caracteres de texto literal no formato MM/DD/AAAA.
ms.assetid: 22c1f9b4-f6c9-4d57-8457-53bb045e2a4d
title: Propriedade Date
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1e4e5cfc7d9236228b9e8b419bbbca48052769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752856"
---
# <a name="date-property"></a>Propriedade Date

A propriedade **Date** é o mês, o dia e o ano atuais como uma cadeia de caracteres de texto literal no formato mm/dd/aaaa. Por exemplo, a data 22 de junho de 2005 pode ser representada como "06/22/2005". O formato do valor depende da localidade do usuário e é o formato obtido usando [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) com a \_ opção Date SHORTDATE. O valor dessa propriedade é definido pelo Windows Installer e não pelo autor do pacote.

## <a name="remarks"></a>Comentários

Como essa é uma cadeia de caracteres de texto, ela não pode ser usada em expressões condicionais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP. Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades](properties.md)
</dt> </dl>

 

