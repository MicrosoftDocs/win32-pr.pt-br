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
ms.openlocfilehash: 2d5a2895e6a0049b2284b55aea1dc9a1849341c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770226"
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

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TPM CIM**](cim-tpm.md)
</dt> </dl>

 

 




