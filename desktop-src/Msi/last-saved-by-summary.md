---
description: O instalador define a última propriedade de resumo salva por Summary com um valor que depende de se esse é um pacote de instalação, uma transformação ou um pacote de patch. Em um pacote de instalação, o instalador define essa propriedade como o valor da propriedade LogonUser durante uma instalação administrativa. Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa para modificar o banco de dados de instalação. Essa propriedade deve ser definida como NULL em um banco de dados de envio final. O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la. Em uma transformação, essa propriedade Summary contém a plataforma e as IDs de idioma que um banco de dados deve ter depois de ter sido transformado. A propriedade especifica para qual o resumo do modelo deve ser definido no novo banco de dados. Em um pacote de patch, essa propriedade de Resumo contém uma lista delimitada por ponto-e-vírgula dos nomes de subarmazenamento de transformação na ordem em que são aplicadas por esse patch.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Última gravação por propriedade de resumo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dfd1c00863eee3bc31728783042ada8298b2067
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778566"
---
# <a name="last-saved-by-summary-property"></a>Última gravação por propriedade de resumo

O instalador define a **última propriedade de resumo salva por Summary** com um valor que depende de se esse é um pacote de instalação, uma transformação ou um pacote de patch.

Em um pacote de instalação, o instalador define essa propriedade como o valor da propriedade [**LogonUser**](logonuser.md) durante uma [instalação administrativa](administrative-installation.md). Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa para modificar o banco de dados de instalação. Essa propriedade deve ser definida como NULL em um banco de dados de envio final. O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la.

Em uma transformação, essa propriedade Summary contém a plataforma e as IDs de idioma que um banco de dados deve ter depois de ter sido transformado. A propriedade especifica para qual o [**Resumo do modelo**](template-summary.md) deve ser definido no novo banco de dados.

Em um pacote de patch, essa propriedade de Resumo contém uma lista delimitada por ponto-e-vírgula dos nomes de subarmazenamento de transformação na ordem em que são aplicadas por esse patch.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições de propriedades de resumo](summary-property-descriptions.md)
</dt> </dl>

 

 




