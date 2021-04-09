---
description: O método getdescriptor retorna o descritor do hub USB conforme especificado pelos parâmetros de entrada.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Método getdescriptor da classe CIM_USBHub (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBHub.GetDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7d68374b4a9267dbc50fbb5b2cd8f1f46018e7f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920291"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a>Método getdescriptor da classe CIM \_ USBHub

O método **getdescriptor** retorna o descritor do hub USB conforme especificado pelos parâmetros de entrada.

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

Identificador mapeado por bit para o tipo de solicitação de descritor e o destinatário. Para obter os valores apropriados para cada bit, consulte a especificação USB.

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

Na entrada, o comprimento (em octetos) do descritor que deve ser retornado. Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado. Se for maior que o comprimento real, o comprimento real será retornado.

Na saída, o comprimento (em octetos) do buffer que está sendo retornado. Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.

</dd> <dt>

*Buffer* \[ fora\]
</dt> <dd>

Buffer retorna as informações de descritor solicitadas. Se o descritor não existir, o conteúdo do buffer será indefinido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 0 (zero) se o descritor de USB for retornado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método. As cadeias de caracteres para as quais os conteúdos de **mofqualifier** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .

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

[**CIM \_ USBHub**](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> </dl>

 

