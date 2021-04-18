---
description: Implementando IWICBitmapCodecProgressNotification (decodificador)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementando IWICBitmapCodecProgressNotification (decodificador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785200"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a>Implementando IWICBitmapCodecProgressNotification (decodificador)

## <a name="iwicbitmapcodecprogressnotification"></a>IWICBitmapCodecProgressNotification

Quando um codec está executando uma operação de e/s como [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) em uma imagem grande, pode levar vários segundos ou até minutos para ser concluído. Quando os usuários finais não conseguem interromper uma operação de execução longa, eles podem imaginar que o aplicativo foi suspenso. Os usuários geralmente fecham um aplicativo ou até mesmo reiniciam seus computadores, em uma tentativa de reobter o controle do computador quando um aplicativo deixa de responder.

Essa interface permite que um aplicativo especifique uma função de retorno de chamada que o codec pode chamar em intervalos especificados para notificar o chamador do progresso da operação atual. O aplicativo pode usar essa função de retorno de chamada para exibir uma indicação de progresso na interface do usuário para notificar o usuário sobre o status da operação. Se um usuário clicar no botão **Cancelar** na caixa de diálogo **progresso** , o aplicativo retornará **WINCODEC \_ erro \_ anulado** da função de retorno de chamada. Quando isso acontece, o codec deve cancelar a operação especificada e propagar esse **HRESULT** de volta para o chamador do método que estava executando a operação.

Essa interface deve ser implementada em sua classe de decodificador de nível de contêiner.


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [RegisterProgressNotification](#registerprogressnotification)
-   [PFNProgressNotification](#pfnprogressnotification)

### <a name="registerprogressnotification"></a>RegisterProgressNotification

[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) é invocado por um aplicativo para registrar uma função de retorno de chamada que o codec pode chamar em intervalos especificados. O primeiro parâmetro, *pfnProgressNotification*, é um ponteiro para a função de retorno de chamada que o codec deve chamar em intervalos regulares.

O parâmetro *pvData* aponta para algum objeto que o chamador deseja que o codec transmita de volta para a função de retorno de chamada sempre que a função de chamada de retorno for invocada. Esse objeto pode ser qualquer coisa e não tem um significado específico para o codec.

O parâmetro *dwProgressFlags* especifica quando o codec deve chamar a função de retorno de chamada. Uma função ou pode ser executada com duas enumerações para esse parâmetro. A enumeração [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) especifica se deve chamar a função de retorno de chamada durante a decodificação (**WICProgressOperationCopyPixels**), codificação (**WICProgerssOperationWritePixels**) ou ambos (**WICProgressOperationAll**).


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



O codec deve chamar a função de retorno de chamada em intervalos regulares durante a operação, mas o chamador pode especificar determinados requisitos. A enumeração [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica em qual ponto da operação chamar a função de retorno de chamada. Se o chamador especificar **WICProgressNotificationBegin**, você deverá chamá-lo no início da operação (0,0). Se o chamador não especificar isso, será opcional. Da mesma forma, se o chamador especificar **WICProgerssNotificationEnd**, você deverá chamá-lo quando a operação for concluída (1,0). Se o chamador especificar **WICProgressNotificationAll**, você deverá chamá-lo no início e no final, bem como em intervalos regulares durante a operação. O chamador também pode especificar **WICProgerssNotificationFrequent**, que indica que eles desejam ser chamados de volta em intervalos frequentes, talvez após cada duas linhas de verificação. (Um chamador geralmente usará esse sinalizador apenas para uma imagem muito grande.) Caso contrário, você normalmente deve chamar de volta em intervalos de aproximadamente 10% de incrementos do número total de linhas de exame a serem processadas.


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



Somente uma função de retorno de chamada por vez pode ser registrada para um decodificador específico ou instância de codificador. Se um aplicativo chamar [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) mais de uma vez, substitua a função de retorno de chamada anteriormente registrada pela nova. Para cancelar um registro de retorno de chamada, um chamador definirá o parâmetro *pfnProgressNotification* como **nulo**.

### <a name="pfnprogressnotification"></a>PFNProgressNotification

[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) é a função de retorno de chamada com a assinatura a seguir.


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



Quando você invoca a função de retorno de chamada, use o parâmetro *pvData* para passar de volta o mesmo *pvData* que o aplicativo especificou quando registrou a função de retorno de chamada.

O parâmetro *uFrameNum* deve indicar o índice do quadro que está sendo processado.

Defina o parâmetro operation como **WICProgressOperationCopyPixels** ao decodificar e **WICProgressOperationWritePixels** ao codificar.

O parâmetro *dblProgress* deve ser um número entre 0,0 (o início da operação) e 1,0 (a conclusão da operação). O valor deve refletir a proporção de linhas de verificação já processadas em relação ao número total de linhas de exame a serem processadas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**ProgressNotificationCallback**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[Implementando IWICBitmapSource](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



