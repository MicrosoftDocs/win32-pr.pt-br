---
description: A \_ classe CIM SupportAccess define como obter assistência para um produto.
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: Classe CIM_SupportAccess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089232"
---
# <a name="cim_supportaccess-class"></a>\_Classe CIM SupportAccess

A classe **CIM \_ SupportAccess** define como obter assistência para um produto.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SupportAccess** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SupportAccess** tem essas propriedades.

<dl> <dt>

**CommunicationInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| FRU \| 2,11 "," MIF. DMTF \| FRU \| 2,12 ")
</dt> </dl>

Detalhes do modo de comunicação. Por exemplo, se a propriedade **communicationmode** é "Phone", essa propriedade especifica o número de telefone a ser chamado.

</dd> <dt>

**Communicationmode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Suporte a DMTF \| \| 1,5 ")
</dt> </dl>

Forma de comunicação a ser usada para obter suporte.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Telefone** (2)


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span id="BBS"></span><span id="bbs"></span>**BBS** (4)


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Serviço online** (5)


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Página da Web** (6)


</dt> <dd>

Página da web

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span id="FTP"></span><span id="ftp"></span>**FTP** (7)


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**Email** (8)


</dt> <dd>

Email

</dd> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Suporte a DMTF \| \| 1,3 ")
</dt> </dl>

Descrição textual do tipo de suporte fornecido.

</dd> <dt>

**Localidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Suporte para DMTF \| 1,2 "), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Região geográfica ou dialeto de idioma ao qual esse recurso de suporte pertence.

</dd> <dt>

**SupportAccessId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Cadeia de caracteres de forma livre arbitrária definida pelo fornecedor do produto ou pela organização que implanta o produto. Essa propriedade, já que é uma chave, deve ser exclusiva em toda a empresa.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

