---
description: Altera a credencial de autorização do proprietário do dispositivo TPM. As senhas de autorização de proprietário antigo e novo são necessárias.
ms.assetid: 5b7f1aec-5181-4330-982c-d80a1d5ae9e8
title: Método ChangeOwnerAuth da classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM.ChangeOwnerAuth
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a92911bcf9c2739d34e8b7602ab5f4cb0032fe5a77376632063971b88f2101d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646658"
---
# <a name="changeownerauth-method-of-the-cim_tpm-class"></a>Método ChangeOwnerAuth da classe CIM \_ TPM

Altera a credencial de autorização do proprietário do dispositivo TPM. As senhas de autorização de proprietário antigo e novo são necessárias.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ChangeOwnerAuth(
  [in] string OldOwnerAuth,
  [in] string NewOwnerAuth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OldOwnerAuth* \[ no\]
</dt> <dd>

Representa a credencial de autorização de proprietário antiga necessária para apropriar-se do dispositivo TPM. A subclasse **CIM \_ SharedCredential** pode ser necessária com um valor não nulo do **\_ SharedCredential CIM**.**Propriedade secreta** para o parâmetro.

</dd> <dt>

*NewOwnerAuth* \[ no\]
</dt> <dd>

Representa a nova credencial de autorização de proprietário necessária para apropriar-se do dispositivo TPM. A subclasse **CIM \_ SharedCredential** pode ser necessária com um valor não nulo do **\_ SharedCredential CIM**.**Propriedade secreta** para o parâmetro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Erro desconhecido/não especificado** (2)
</dt> <dt>

**DMTF reservado** (3.. 4095)
</dt> <dt>

**Método reservado** (4096.. 32767)
</dt> <dt>

**Fornecedor especificado** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




