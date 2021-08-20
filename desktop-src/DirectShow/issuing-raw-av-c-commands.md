---
description: Emitindo comandos AV/C brutos
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emitindo comandos AV/C brutos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729cad0be3a55a3f95592e54e8f91b9074892a8d111da9ad996b4e00a136cbe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153783"
---
# <a name="issuing-raw-avc-commands"></a>Emitindo comandos AV/C brutos

As interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)e [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funcionam convertendo as chamadas de método em comandos para o driver e, em seguida, interpretando a resposta do driver e retornando-a por meio de um parâmetro **HRESULT** ou output. No entanto, algumas funções de dispositivo podem não estar acessíveis por meio desses métodos. Portanto, o MSDV dá suporte ao envio de comandos AV/C brutos para o dispositivo.

Você deve ter os seguintes pontos em mente ao usar esse recurso:

-   O comando é passado diretamente para o dispositivo, sem verificação de erro ou validação de parâmetro. por esse motivo, você deve emitir comandos AV/C brutos somente quando as interfaces de DirectShow não implementam a funcionalidade de que você precisa.
-   Todos os comandos AV/C brutos são síncronos. O thread que emite os blocos de comando até que o comando retorne.
-   Apenas um comando pode ser fornecido por vez. Enquanto o comando estiver sendo processado, o dispositivo rejeitará todos os comandos adicionais.
-   O driver UVC não dá suporte a comandos brutos AV/C.

Para enviar um comando AV/C, formate o comando como uma matriz de bytes. Em seguida, chame [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters). Passe o sinalizador de \_ cmd de dev ext brutos Ed \_ \_ \_ , o tamanho da matriz e a matriz. Você deve converter o endereço da matriz em um tipo **LPOLESTR \*** , pois a finalidade original desse parâmetro era retornar um valor de cadeia de caracteres.


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR*) AvcCmd);
```



O conteúdo da matriz é passado diretamente para o dispositivo, portanto, você deve ter cuidado para formatá-lo corretamente. Um comando pode direcionar a unidade (camcorder) ou uma subunidade (fita ou câmera). Os padrões relevantes estão disponíveis no [site da associação comercial 1394](https://1394ta.org).

-   Especificação geral do comando de interface digital AV/C
-   Especificação de subunidade do gravador de fita AV/C/Player

A primeira descreve como formatar comandos AV/C e lista os comandos de unidade. A segunda especificação lista os comandos de subunidade.

O método **GetTransportBasicParameters** pode retornar um dos seguintes códigos de erro:



| Código do Erro              | Descrição                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| \_tempo limite do erro          | O tempo limite do comando foi atingido.                                                           |
| Req. de erro \_ \_ não \_ ACCEP  | O dispositivo não aceitou o comando.                                           |
| ERRO \_ sem \_ suporte   | O dispositivo não oferece suporte ao comando.                                         |
| solicitação de erro \_ \_ anulada | O comando foi anulado. Possbly o dispositivo foi removido ou uma redefinição de barramento ocorreu. |



 

> [!Note]  
> Esses erros são retornados como códigos de erro do Win32, não HRESULTs, portanto, você deve testar esses valores diretamente, em vez de usar as macros com **êxito** e **com falha** .

 

Se o método retornar S \_ OK, a resposta do dispositivo será copiada para a matriz. A carga de resposta pode ser maior que o comando, portanto, você deve alocar um buffer grande o suficiente para contê-lo. O tamanho máximo da carga é de 512 bytes. Observe que um valor de retorno de S \_ OK nem sempre significa que o dispositivo realizou o comando com êxito. O aplicativo deve examinar a carga de resposta para determinar o status.

O exemplo a seguir mostra o comando para procurar uma pesquisa de número de faixa absoluta:


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



