---
description: Especifica o CSP (provedor de serviços de criptografia) e as informações de chave privada usadas para criar uma assinatura digital.
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: Estrutura de SIGNER_PROVIDER_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 02cf4be124dd2ba1f39695bd5ca34af012cf7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778669"
---
# <a name="signer_provider_info-structure"></a>Estrutura de informações do \_ provedor de assinante \_

A estrutura de **\_ \_ informações do provedor de assinante** especifica o CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) e as informações de chave privada usadas para criar uma assinatura digital.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho, em bytes, da estrutura.

</dd> <dt>

**pwszProviderName**
</dt> <dd>

O nome do CSP usado para criar a assinatura digital. Se o valor desse membro for **nulo**, o provedor padrão será usado.

</dd> <dt>

**dwProviderType**
</dt> <dd>

O tipo de CSP especificado pelo membro **pwszProviderName** .

</dd> <dt>

**dwKeySpec**
</dt> <dd>

A especificação de chave. Se esse membro for definido como zero, a especificação de chave no membro **pwszPvkFileName** ou **pwszKeyContainer** será usada. Se houver mais de uma especificação de chave no membro **pwszKeyContainer** , **a \_ assinatura** será usada. Se falhar, **em \_ keyexchange** será usado.

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

Especifica o tipo de informações de chave privada. Esse membro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                                               | Significado                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_ Digite \_ o \_ nome do arquivo**</dt> <dt>1 (0x1)</dt> </dl>         | As informações de chave privada são um nome de arquivo.<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_ Digite \_ keycontainer**</dt> <dt>2 (0x2)</dt> </dl> | As informações de chave privada são um contêiner de chave.<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

O nome do arquivo que contém as informações de chave privada.

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

O nome do contêiner de chave que contém as informações de chave privada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
