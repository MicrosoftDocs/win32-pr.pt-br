---
title: SoHAttributeValue Union (NapProtocol. h)
description: Define o conteúdo do membro de tipo em uma estrutura SoHAttribute.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- NAP do SoHAttributeValue Union
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455721"
---
# <a name="sohattributevalue-union"></a>SoHAttributeValue Union

> [!Note]  
> A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10

 

A União **SoHAttributeValue** define o conteúdo do membro de **tipo** em uma estrutura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) . A estrutura da União **SoHAttributeValue** é determinada pelo [**SoHAttributeType**](sohattributetype-enum.md) especificado no membro de **tipo** da estrutura [**SoHAttribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) .

## <a name="syntax"></a>Sintaxe


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a>Membros

<dl> <dt>

**idVal**
</dt> <dd>

**caso (sohAttributeTypeSystemHealthId)**

Um [SystemHealthEntityId](nap-datatypes.md) exclusivo que contém a ID do Sha (agente de integridade do sistema) ou o SHV (validador da integridade do sistema) que construiu este pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) .

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**caso (sohAttributeTypeIpv4FixupServers)**

Os endereços IPv4 dos servidores de correção em uso pelo sistema NAP.

<dl> <dt>

**contagem**
</dt> <dd>

O número de endereços IPv4 no membro de **endereços** no intervalo de 1 a [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**atende**
</dt> <dd>

Uma matriz de estruturas [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) que contêm os endereços IPv4.

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**caso (sohAttributeTypeIpv6FixupServers)**

Os endereços IPv6 dos servidores de correção em uso pelo sistema NAP.

<dl> <dt>

**contagem**
</dt> <dd>

O número de endereços IPv4 no membro de **endereços** no intervalo de 1 a [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**atende**
</dt> <dd>

Uma matriz de estruturas [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) que contêm os endereços IPv4.

</dd> </dl> </dd> <dt>

**codesVal**
</dt> <dd>

**caso (sohAttributeTypeComplianceResultCodes, sohAttributeTypeErrorCodes)**

Uma estrutura [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) que contém os códigos de resultado de conformidade definidos pelo aplicativo das [**constantes de erro**](nap-error-constants.md)do cliente ou NAP. Um pacote [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) deve conter esse TLV ou o TLV **sohAttributeTypeFailureCategory** .

</dd> <dt>

**dateTimeVal**
</dt> <dd>

**caso (sohAttributeTypeTimeOfLastUpdate, sohAttributeTypeSoHGenerationTime)**

Uma estrutura [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) que contém a hora da última atualização [**soh**](/windows/win32/api/naptypes/ns-naptypes-soh) ou o tempo de geração **soh** .

</dd> <dt>

**vendorSpecificVal**
</dt> <dd>

**caso (sohAttributeTypeVendorSpecific)**

Dados específicos do aplicativo que são definidos pelo fornecedor.

<dl> <dt>

**vendorId**
</dt> <dd>

Um identificador de 4 bytes que define a ID do par de SHA/SHV. Os três primeiros bytes são o código de SMI atribuído pela IETF do fornecedor e o último byte identifica o próprio componente. Ao implementar um SHA ou SHV, não use os valores de ID atribuídos aos componentes internos da integridade do sistema da Microsoft nas [**constantes do fornecedor NAP**](nap-vendor-constants.md).

</dd> <dt>

**size**
</dt> <dd>

O tamanho, em bytes, dos dados do fornecedor no intervalo de 0 a ([**maxSoHAttributeSize**](nap-type-constants.md) -4).

</dd> <dt>

**vendorSpecificData**
</dt> <dd>

Um ponteiro para os dados específicos do fornecedor na ordem de bytes da rede.

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**Case (sohAttributeTypeHealthClass, sohAttributeTypeFailureCategory, sohAttributeTypeExtendedIsolationState)**

A classe de integridade, a categoria de falha ou o estado de isolamento estendido de um componente NAP como um valor [**HealthClassValue**](healthclassvalue-enum.md) ou [**FailureCategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) ou uma estrutura [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) .

</dd> <dt>

**octetStringVal**
</dt> <dd>

**default**

Os seguintes valores de atributos são cadeias de caracteres de octeto:

-   sohAttributeTypeSoftwareVersion
-   sohAttributeTypeClientId
-   sohAttributeTypeProductName
-   sohAttributeTypeHealthClassStatus

Para compatibilidade com o encaminhamento, todos os atributos não reconhecidos são retornados como cadeias de caracteres de octeto. **os dados** devem estar na ordem de bytes da rede.

<dl> <dt>

**size**
</dt> <dd>

O tamanho, em bytes, dos **dados** no intervalo de 0 a [**maxSoHAttributeSize**](nap-type-constants.md).

</dd> <dt>

**data**
</dt> <dd>

Um ponteiro para o valor da cadeia de caracteres do octeto.

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>Layout de dados real

Devido à natureza do ambiente de publicação do SDK, as uniões não são claramente representadas em blocos de sintaxe. Aqui está a sintaxe real do arquivo de cabeçalho NapProtocol. h.


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a>Comentários

Esses tipos de atributo são consumidos pelo sistema NAP:

-   sohAttributeTypeSystemHealthId
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohAttributeTypeComplianceResultCodes
-   sohAttributeTypeFailureCategory

O restante dos [**SoHAttributeTypes**](sohattributetype-enum.md) são apenas uma orientação prescritiva para uso por SHAs e SHVs.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>NapProtocol. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>NapProtocol. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência de NAP](nap-reference.md)
</dt> <dt>

[Estruturas de NAP](nap-structures.md)
</dt> </dl>

 

