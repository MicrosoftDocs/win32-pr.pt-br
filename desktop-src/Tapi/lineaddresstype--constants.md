---
description: O tipo de endereço identifica o formato de endereço, como número de telefone padrão ou endereço de email. Somente aplicativos que negociam TAPI versão 3.0 ou superior podem usar tipos de endereço.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: LINEADDRESSTYPE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6555ff934ffb8c1b40b8f35d279a2071cad32b80b754af19672108f5e318a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873326"
---
# <a name="lineaddresstype_-constants"></a>Constantes LINEADDRESSTYPE \_

O tipo de endereço identifica o formato de endereço, como número de telefone padrão ou endereço de email. Somente aplicativos que negociam TAPI versão 3.0 ou superior podem usar tipos de endereço.

<dl> <dt>

<span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



O tipo de endereço é um número de telefone padrão.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE \_ SDP**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



O tipo de endereço é a conferência SDP (Protocolo de Descrição da Sessão).


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Tipo de endereço é um nome de email.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



O tipo de endereço é um nome de domínio.


</dt> </dl> </dd> <dt>

<span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE \_ IPADDRESS**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



O tipo de endereço é um endereço IP.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.0 ou posterior<br/>                                             |
| Cabeçalho<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




