---
description: O método getdescriptor retorna o descritor de dispositivo USB conforme especificado pelos parâmetros de entrada.
ms.assetid: 5f36ac8a-e751-4494-b91e-c6733bc3e349
ms.tgt_platform: multiple
title: Método getdescriptor da classe CIM_USBDevice (Wmcodecdsp. h)
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
- CIMWin32.dll
ms.openlocfilehash: 35ce9a83efb580d6e5e44f55a01182e7390c120e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755198"
---
# <a name="getdescriptor-method-of-the-cim_usbdevice-class-wmcodecdsph"></a>Método getdescriptor da classe CIM_USBDevice (Wmcodecdsp. h)

O método **getdescriptor** retorna o descritor de dispositivo USB conforme especificado pelos parâmetros de entrada.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

Identificador mapeado por bit para o tipo de solicitação de descritor e o destinatário. Consulte a especificação USB para obter os valores apropriados para cada bit.

</dd> <dt>

*RequestValue* \[ no\]
</dt> <dd>

Contém o tipo de descritor no alto byte e o índice de descritor (por exemplo, index ou offset na matriz de descritores) no byte baixo. Para obter mais informações, consulte a especificação USB.

</dd> <dt>

*RequestIndex* \[ no\]
</dt> <dd>

Especifica o código do identificador de idioma de 2 bytes usado pelo dispositivo USB ao retornar dados do descritor de cadeia de caracteres. Normalmente, o parâmetro é 0 (zero) para descritores que não são de cadeia de caracteres. Para obter mais informações, consulte a especificação USB.

</dd> <dt>

*RequestLength* \[ entrada, saída\]
</dt> <dd>

Na entrada, comprimento (em octetos) do descritor que deve ser retornado. Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado. Se for maior que o comprimento real, o comprimento real será retornado.

Na saída, o comprimento (em octetos) do buffer que está sendo retornado. Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.

</dd> <dt>

*Buffer* \[ fora\]
</dt> <dd>

Retorna as informações de descritor solicitadas. Se o descritor não existir, o conteúdo desse parâmetro será indefinido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se o descritor de USB for retornado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método. As cadeias de caracteres para as quais os conteúdos de mofqualifier são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .

## <a name="remarks"></a>Comentários

Este método não está implementado no momento pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_USBDEVICE CIM**](getdescriptor-method-in-class-cim-usbdevice.md)
</dt> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> </dl>

 

