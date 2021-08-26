---
description: Retorna o descritor USBDevice conforme especificado pelos parâmetros de entrada.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Método GetDescriptor da classe CIM_USBDevice (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice.GetDescriptor
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d0523cc88205792f9429eb1a214d8b74a1ca4c2f2bf35813c25614f9f3c06199
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980776"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>Método GetDescriptor da classe CIM_USBDevice (gerenciamento do Hyper-V)

Retorna o descritor USBDevice conforme especificado pelos parâmetros de entrada.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetDescriptor(
  [in]      uint8  RequestType,
  [in]      uint16 RequestValue,
  [in]      uint16 RequestIndex,
  [in, out] uint16 RequestLength,
  [out]     uint8  Buffer[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RequestType* \[ Em\]
</dt> <dd>

Mapa de bits que identifica o tipo de solicitação do Descritor e o destinatário. O tipo de solicitação pode ser 'standard', 'class' ou 'vendor-specific'. O destinatário pode ser 'device', 'interface', 'endpoint' ou 'other'. Consulte a Especificação USB para ver os valores apropriados para cada bit.

</dd> <dt>

*RequestValue* \[ Em\]
</dt> <dd>

Contém o Tipo de Descritor no byte alto e o Índice do Descritor (por exemplo, índice ou deslocamento na matriz descritor) no byte baixo. Consulte a Especificação USB para obter mais informações.

</dd> <dt>

*RequestIndex* \[ Em\]
</dt> <dd>

Define o código de ID da Linguagem de 2 byte usado pelo USBDevice ao retornar dados do Descritor de cadeia de caracteres. O parâmetro normalmente é 0 para Descritores que não são de cadeia de caracteres. Consulte a Especificação USB para obter mais informações.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

Na entrada, contém o comprimento (em octetos) do Descritor que deve ser retornado. Se esse valor for menor que o tamanho real do Descritor, somente o comprimento solicitado será retornado. Se for maior que o tamanho real, o comprimento real será retornado. Na saída, esse parâmetro é o comprimento, em octetos, do Buffer que está sendo retornado. Se o Descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.

</dd> <dt>

*Buffer* \[ out\]
</dt> <dd>

Retorna as informações de descritor solicitadas. Se o Descritor não existir, o conteúdo do parâmetro será indefinido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> </dl>

 

 




