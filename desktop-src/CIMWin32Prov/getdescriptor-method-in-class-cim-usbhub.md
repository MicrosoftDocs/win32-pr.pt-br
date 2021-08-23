---
description: O método GetDescriptor retorna o descritor do hub USB conforme especificado pelos parâmetros de entrada.
ms.assetid: 0090da35-0de1-4ea5-b983-bd9bf9997009
ms.tgt_platform: multiple
title: Método GetDescriptor da classe CIM_USBHub (Wmcodecdsp.h)
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
ms.openlocfilehash: 5253f0eae0acf8844e844f5bfb48fcd73b2b186c6537dfcfcb0da5fb8f46582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879046"
---
# <a name="getdescriptor-method-of-the-cim_usbhub-class"></a>Método GetDescriptor da classe CIM \_ USBHub

O **método GetDescriptor** retorna o descritor do hub USB conforme especificado pelos parâmetros de entrada.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

Este tópico usa sintaxe Managed Object Format (MOF). Para obter mais informações sobre como usar esse método, consulte [Chamando um método](/windows/desktop/WmiSdk/calling-a-method).

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

Identificador mapeado em bit para o tipo de solicitação de descritor e o destinatário. Para os valores apropriados para cada bit, consulte a especificação USB.

</dd> <dt>

*RequestValue* \[ Em\]
</dt> <dd>

Contém o tipo de descritor no byte alto e no índice do descritor (por exemplo, índice ou deslocamento na matriz do descritor) no byte baixo. Para obter mais informações, consulte a especificação USB.

</dd> <dt>

*RequestIndex* \[ Em\]
</dt> <dd>

Especifica o código do identificador de idioma de 2 byte usado pelo dispositivo USB ao retornar dados do descritor de cadeia de caracteres. O parâmetro normalmente é 0 (zero) para descritores nãostring. Para obter mais informações, consulte a especificação USB.

</dd> <dt>

*RequestLength* \[ in, out\]
</dt> <dd>

Na entrada, o comprimento (em octetos) do descritor que deve ser retornado. Se esse valor for menor que o comprimento real do descritor, somente o comprimento solicitado será retornado. Se for maior que o tamanho real, o comprimento real será retornado.

Na saída, o comprimento (em octetos) do buffer que está sendo retornado. Se o descritor solicitado não existir, o conteúdo desse parâmetro será indefinido.

</dd> <dt>

*Buffer* \[ out\]
</dt> <dd>

O buffer retorna as informações de descritor solicitadas. Se o descritor não existir, o conteúdo do buffer será indefinido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um valor de 0 (zero) se o descritor USB for retornado com êxito, 1 (um) se a solicitação não tiver suporte e qualquer outro número para indicar um erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método . As cadeias de caracteres para as quais o conteúdo **do mofqualifier** são convertidos também podem ser especificadas na subclasse como um qualificador **da** matriz Valores.

## <a name="remarks"></a>Comentários

Atualmente, esse método não é implementado pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ USBHub**](getdescriptor-method-in-class-cim-usbhub.md)
</dt> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> </dl>

 

