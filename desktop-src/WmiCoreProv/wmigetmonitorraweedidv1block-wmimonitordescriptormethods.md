---
description: Obtém os dados brutos de uma estrutura E-EDID (dados de identificação de exibição estendida) avançada da VESA (Standard Electronics data Identification) que define as configurações ideais para configurar um monitor.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Método WmiGetMonitorRawEEdidV1Block da classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765259"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>Método WmiGetMonitorRawEEdidV1Block da classe WmiMonitorDescriptorMethods

O método **WmiGetMonitorRawEEdidV1Block** Obtém os dados brutos de uma estrutura E-EDID (dados de identificação de exibição estendida) avançada da VESA (Standard Electronics data Identification) que define as configurações ideais para configurar um monitor.

## <a name="syntax"></a>Sintaxe


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Blockid* \[ no\]
</dt> <dd>

A identidade do bloco de dados.

</dd> <dt>

*BlockType* \[ fora\]
</dt> <dd>

Tipo de bloco de dados. A tabela a seguir lista os possíveis valores de retorno.



| Valor                                                                                 | Significado                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | Não Inicializado<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Bloco base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mapa de bloco EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Outro<br/>           |



 

</dd> <dt>

*BlockContent* \[ fora\]
</dt> <dd>

Uma matriz de 128 bytes que contém o conteúdo de bloco bruto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna zero (0) para indicar êxito. Qualquer outro número indica um erro. Para obter mais informações sobre códigos de erro, consulte [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir recupera os blocos EDID de qualquer exibição como matrizes de bits de 128 brutos.


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

