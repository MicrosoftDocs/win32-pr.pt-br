---
description: Método StartService da classe CIM_Service (provedores WMI CIMWin32)-o método StartService coloca o serviço em um estado iniciado.
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Método StartService da classe CIM_Service (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87fcdad650ea93461850bab3e3e66d9543025a2b468b9f7948f6d949d5838c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752436"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a>Método StartService da classe CIM_Service (provedores WMI CIMWin32)

O método **StartService** coloca o serviço em um estado iniciado.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Este tópico usa a sintaxe formato MOF (MOF). Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxe


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro. Em uma subclasse, o conjunto de códigos de retorno possíveis pode ser especificado usando um qualificador **ValueMap** no método. As cadeias de caracteres nas quais os conteúdos de **ValueMap** são convertidos também podem ser especificadas na subclasse como um qualificador de matriz de **valores** .

## <a name="remarks"></a>Comentários

Este método não está implementado no momento pelo WMI. Para usar esse método, você deve implementá-lo em seu próprio provedor.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[\_Serviço CIM](startservice-method-in-class-cim-service.md)
</dt> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

