---
description: Usado para configurar componentes CAPICOM.
title: Objeto de configurações
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762010"
---
# <a name="settings-object-cryptography"></a>Objeto Settings (criptografia)

\[O objeto de **configurações** está disponível para uso nos sistemas operacionais especificados na seção requisitos.\]

O objeto **Settings** é usado para configurar os componentes CAPICOM.

## <a name="members"></a>Membros

O objeto de **configurações** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

O objeto **Settings** tem essas propriedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriedade</th>
<th style="text-align: left;">Tipo de acesso</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Define ou recupera o local de pesquisa do Active Directory. O local inicial não é especificado por padrão. Quando o local não é especificado, o catálogo global é pesquisado e, em seguida, o domínio padrão é pesquisado. A pesquisa determina se o atributo de certificado do usuário é publicado nesse local.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Define ou recupera um valor booliano que indica se os prompts de interface do usuário para uma identidade de signatário ou remetente podem ser usados. <br/>
<blockquote>
[!Note]<br />
Definir essa propriedade não desabilita os avisos gerados antes de qualquer uso de chave privada ser feito de um aplicativo baseado na Web.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

O objeto de **configurações** pode ser criado e é seguro para scripts. O ProgID do objeto de **configurações** é CAPICOM. Configurações. 1.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuível<br/> | CAPICOM 2,0 ou posterior no Windows Server 2003 e no Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> </dl>

 

 




