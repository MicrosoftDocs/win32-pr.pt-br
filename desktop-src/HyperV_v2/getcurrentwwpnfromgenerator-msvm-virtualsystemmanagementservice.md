---
description: Fornece a capacidade de visualizar o WWPN (World Wide Port Name) atual sem o WWPN sendo reservado.
ms.assetid: 7fc02099-744e-4a56-ae4b-1f5fd6a1eb45
title: Método GetCurrentWwpnFromGenerator da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetCurrentWwpnFromGenerator
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 196ad781075128eab42c6daabf7d6ccd6906df1e67e348ebea0d9418cbb08c24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393278"
---
# <a name="getcurrentwwpnfromgenerator-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetCurrentWwpnFromGenerator da \_ classe VirtualSystemManagementService Msvm

Fornece a capacidade de visualizar o WWPN (World Wide Port Name) atual sem o WWPN sendo reservado. O WWPN é gerado de dentro do intervalo pré-configurado definido pelas propriedades **MinimumWWPNAddress** e **MaximumWWPNAddress** da classe [**Msvm \_ VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) . Se o intervalo definido por essas propriedades for esgotado, o WWPN gerado terá a entrada inválida de "0000000000000000" e o valor de retorno indicará êxito (0).

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetCurrentWwpnFromGenerator(
  [out] string CurrentWwpn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CurrentWwpn* \[ fora\]
</dt> <dd>

Uma cadeia de caracteres que terá o valor do WWPN atual, conforme usado pelo gerador de WWPN. Esse será o mesmo valor que será o primeiro WWPN gerado pela chamada subsequente para [**GenerateWwpn**](generatewwpn-msvm-virtualsystemmanagementservice.md). Ele será formatado em formato de cadeia de caracteres como "01:23:45:67:89: AB: CD: EF".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




