---
description: O instalador define a propriedade Last Saved by Summary como um valor que depende se este é um pacote de instalação, transformação ou pacote de patch. Em um pacote de instalação, o instalador define essa propriedade como o valor da propriedade LogonUser durante uma instalação administrativa. Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa a modificar o banco de dados de instalação. Essa propriedade deve ser definida como Null em um banco de dados de envio final. O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la. Em uma transformação, essa propriedade de resumo contém as IDs de plataforma e idioma que um banco de dados deve ter depois de ser transformado. A propriedade especifica como o Resumo do Modelo deve ser definido no novo banco de dados. Em um pacote de patch, essa propriedade de resumo contém uma lista delimitada por ponto e vírgula de nomes de substorage de transformação na ordem em que são aplicados por esse patch.
ms.assetid: 6da171d9-29db-4524-abc6-77db8fbfca38
title: Propriedade Last Saved By Summary
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9299dc6a00af4e48eb3901842aba58a3c8d9a9c1d98d3a3e1e0f05bfccc4333
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979446"
---
# <a name="last-saved-by-summary-property"></a>Propriedade Last Saved By Summary

O instalador define a **propriedade Last Saved by Summary** como um valor que depende se este é um pacote de instalação, transformação ou pacote de patch.

Em um pacote de instalação, o instalador define essa propriedade como o valor da [**propriedade LogonUser**](logonuser.md) durante uma [instalação administrativa](administrative-installation.md). Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa a modificar o banco de dados de instalação. Essa propriedade deve ser definida como Null em um banco de dados de envio final. O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la.

Em uma transformação, essa propriedade de resumo contém as IDs de plataforma e idioma que um banco de dados deve ter depois de ser transformado. A propriedade especifica como o Resumo [**do Modelo**](template-summary.md) deve ser definido no novo banco de dados.

Em um pacote de patch, essa propriedade de resumo contém uma lista delimitada por ponto e vírgula de nomes de substorage de transformação na ordem em que são aplicados por esse patch.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Descrições da propriedade Summary](summary-property-descriptions.md)
</dt> </dl>

 

 




