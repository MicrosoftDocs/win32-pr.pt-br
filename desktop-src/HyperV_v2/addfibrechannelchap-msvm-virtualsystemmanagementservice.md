---
description: Adiciona parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a uma porta de Fibre Channel sintética em uma máquina virtual.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Método AddFibreChannelChap da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921787"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddFibreChannelChap da \_ classe VirtualSystemManagementService Msvm

Adiciona parâmetros DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a uma porta de Fibre Channel sintética em uma máquina virtual. Esse método falhará se a máquina virtual estiver em execução.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*FcPortSettings* \[ no\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) que descreve as configurações de portas Fibre Channel sintéticas para máquinas virtuais. A propriedade **InstanceId** de cada uma dessas instâncias identifica os elementos a serem modificados.

</dd> <dt>

*SecretEncoding* \[ no\]
</dt> <dd>

Especifica o tipo de codificação para o segredo compartilhado.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**ASCII imprimível** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binário** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SharedSecret* \[ no\]
</dt> <dd>

Especifica o segredo compartilhado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




