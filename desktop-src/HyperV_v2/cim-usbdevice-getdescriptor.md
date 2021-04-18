---
description: Retorna o descritor USBDevice conforme especificado pelos parâmetros de entrada.
ms.assetid: 89bb8a49-6fca-422c-808d-70ae77aae4c3
title: Método getdescriptor da classe CIM_USBDevice (gerenciamento do Hyper-V)
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
ms.openlocfilehash: f6aa8e7dc37f2bb7fe48ce0293bbaad9663150dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756770"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-hyper-v-management"></a>Método getdescriptor da classe CIM_USBDevice (gerenciamento do Hyper-V)

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

*RequestType* \[ no\]
</dt> <dd>

Mapa de bits que identifica o tipo de solicitação de descritor e o destinatário. O tipo de solicitação pode ser ' padrão ', ' classe ' ou ' específico do fornecedor '. O destinatário pode ser ' dispositivo ', ' interface ', ' ponto de extremidade ' ou ' outros '. Consulte a especificação USB para obter os valores apropriados para cada bit.

</dd> <dt>

*RequestValue* \[ no\]
</dt> <dd>

Contém o tipo de descritor no alto byte e o índice de descritor (por exemplo, index ou offset na matriz de descritores) no byte baixo. Consulte a especificação USB para obter mais informações.

</dd> <dt>

*RequestIndex* \[ no\]
</dt> <dd>

Define o código de ID de idioma de 2 bytes usado pelo USBDevice ao retornar dados de descritor de cadeia de caracteres. O parâmetro geralmente é 0 para descritores que não são de cadeia de caracteres. Consulte a especificação USB para obter mais informações.

</dd> <dt>

*RequestLength* \[ entrada, saída\]
</dt> <dd>

Na entrada, contém o comprimento (em octetos) do descritor que deve ser retornado. Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado. Se for maior que o comprimento real, o comprimento real será retornado. Na saída, esse parâmetro é o comprimento, em octetos, do buffer que está sendo retornado. Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.

</dd> <dt>

*Buffer* \[ fora\]
</dt> <dd>

Retorna as informações de descritor solicitadas. Se o descritor não existir, o conteúdo do parâmetro será indefinido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

 




